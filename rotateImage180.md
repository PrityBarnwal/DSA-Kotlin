# Rotate Image 180 degree

## OverView

```ruby
fun rotateImage(image:Array<IntArray>){
    val n =image.size
    var startRow =0
    var endRow =n-1
    while(startRow < endRow){
        val temp = image[startRow]
        image[startRow] = image[endRow]
        image[endRow] = temp
        startRow++
        endRow--
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

    println("\nRotated Image (180 degrees clockwise):")
    printImage(image)
}
```
# Input/Output
```ruby
Original Image:
1 2 3
4 5 6
7 8 9

Rotated Image (180 degrees clockwise):
9 8 7
6 5 4
3 2 1
```