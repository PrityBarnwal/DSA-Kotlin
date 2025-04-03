```ruby
fun main() {
    val numbers = intArrayOf(1, 0, 2, 3, 4, 5, 7, 9, 0, 6)
    println("${moveZerosAtEnd(numbers).joinToString(", ")}") 
}

fun moveZerosAtEnd(nums:IntArray):IntArray{
    var index = 0
	for(num in nums){
   	 if(num != 0){
        nums[index] = num
        index++
   	 }
	}
    while(index < nums.size){
        nums[index] = 0
        index++
    }
    return nums
}
```
## Output
1, 2, 3, 4, 5, 7, 9, 6, 0, 0
