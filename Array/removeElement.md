# Remove Element
## Overview

```ruby
fun removeElement(nums:IntArray,`val`:Int):Int{
    var k = 0
    for(i in nums.indices){
        if(nums[i] != `val`){
            nums[k] = nums[i]
            k++
        }
    }
    return k
}
```

```ruby
fun main(){
    val nums = intArrayOf(3,2,2,3,4,5,3)
    val len =removeElement(nums,3) 
    println("New length $len")
    println("Modified array ${nums.slice(0 until len)}")
}
```

## Output

```ruby
New length 4
Modified array [2, 2, 4, 5]
```