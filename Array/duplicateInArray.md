# Duplicate Array

## OverView

```ruby
fun duplicate(nums:IntArray):Int?{
    val n = nums.size
    for(i in 0 until n){
        for(j in i+1 until n){
            if(nums[i] == nums[j]){
               return nums[i]
            }
        }
    }
     return null
}
```
```ruby
fun main() {
    val array = intArrayOf(1, 2, 3,5,6,8,6)
    val result = duplicate(array)

    if (result != null) {
        println("First duplicate found: $result")
    } else {
        println("No duplicates found.")
    }
   
}
```

# Input/Output

```ruby
First duplicate found: 6
```