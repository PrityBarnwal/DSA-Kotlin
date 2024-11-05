  # Misssing Number
  ## Function and Implementation
   ```ruby
   fun findMissingNumber(nums:IntArray):Int{
        val n = nums.size
        val expectedSum = n*(n+1)/2
        val actualsum = nums.sum()
        return expectedSum -actualsum
    }
```
    
```ruby
fun main() {
    val nums = intArrayOf(3, 0, 1) // Example input
    val missingNumber = findMissingNumber(nums)
    println("The missing number is: $missingNumber") // Output: 2
}
```