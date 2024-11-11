# Move Zeros at End
## Overview

```ruby
fun moveZeroes(nums:IntArray){
    var lastNonZerosIndex=0 // Pointer to track where the next non-zero element should go

   // Move all non-zero elements to the front
    for(i in nums.indices){
        if(nums[i] !=0){
            nums[lastNonZerosIndex] =nums[i]
            if(i != lastNonZerosIndex){
                nums[i] = 0
            }
            lastNonZerosIndex++
        }
    }
}
```
```ruby
fun main() {
    val nums = intArrayOf(0, 1, 0, 3, 12)
    moveZeroes(nums)
    println(nums.joinToString(", "))  // Output: 1, 3, 12, 0, 0
}
```
# Output
```ruby
1, 3, 12, 0, 0
```