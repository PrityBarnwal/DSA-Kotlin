# Single Number
## Overview

```ruby
fun singleNumber(nums:IntArray):Int{
    var result = 0
    for(num in nums){
        result = result xor num
        //or result ^= num 
    }
    return result
}
```
```ruby
fun main() {
    val nums = intArrayOf(4, 1, 2, 1, 2)
    println("single number in array -> ${singleNumber(nums")  
}
```

# Output
```ruby
single number in array -> 4
```