# Rotate Image 90 degree

## OverView

```ruby
fun rotateImage(image:Array<IntArray>){
    val n =image.size
    for(i in 0 until n){
        for(j in i until n){
            val temp = image[i][j]
            image[i][j] =image[j][i]
            image[j][i] = temp
        }
    }
    for(i in 0 until n){
        var start = 0
        var end = n-1
        while(start<end){
            val temp = image[i][start]
            image[i][start] = image[i][end]
            image[i][end] = temp
            start++
            end--
        }
    }
}
```
```ruby
fun printImage(image: Array<IntArray>) {
    for (row in image) {
        println(row.joinToString(" "))
    }
}
```
```ruby
fun main() {
    val image = arrayOf(
        intArrayOf(1, 2, 3),
        intArrayOf(4, 5, 6),
        intArrayOf(7, 8, 9)
    )

    println("Original Image:")
    printImage(image)

    rotateImage(image)

    println("\nRotated Image (90 degrees clockwise):")
    printImage(image)
}
```

# Input/Output
```ruby
Original Image:
1 2 3
4 5 6
7 8 9

Rotated Image (90 degrees clockwise):
7 4 1
8 5 2
9 6 3
```