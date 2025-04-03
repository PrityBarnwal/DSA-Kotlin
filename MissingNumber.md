```ruby
fun main() {
    val numbers = intArrayOf(1, 2,3, 4, 5,7)
    println("${missingNumber(numbers)}") 
}

fun missingNumber(nums:IntArray):Int{
    var n = nums.size-1
    for(i in 0 until n){
        if(nums[i+1]-nums[i] > 1){
            return nums[i]+1
        }
    }
    return -1
}
```
## Output
6
