# Reverse String
## Overview
```ruby
fun reverseArray(arr:IntArray){
    var left = 0
    var right = arr.size -1
    while(left< right){
    val temp = arr[left]
    arr[left]= arr[right]
    arr[right] = temp
    left++
    right--
    }
}
```
```ruby
fun main() {
    val arr = intArrayOf(1, 2, 3, 4, 5)
    reverseArrayInPlace(arr)
    println("Reversed Array: ${arr.joinToString()}")
}
```

## Output
```ruby
Reversed Array: 5, 4, 3, 2, 1
```