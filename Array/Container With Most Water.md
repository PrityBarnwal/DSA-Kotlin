# Container With Most Water

## Overview
	Find two lines that together with the x-axis form a container, such that the container contains the most water.
	Return the maximum amount of water a container can store.

## Function and Implementations

```ruby
	fun maxArea(height:IntArray):Int{
    var left =0
    var right = height.size -1
    var maxArea =0
    
    while(left < right){
       val width = right -left
        val currentHeight = minOf(height[left],height[right])
        val currentArea = width * currentHeight
        maxArea= maxOf(maxArea,currentArea)
        
        if(height[left] < height[right]){
            left++
        }else{
            right--
        }
    }
    return maxArea
}
```
```ruby
fun main() {
    val arr = intArrayOf(1,8,6,2,5,4,8,3,7)
    val result = maxArea(arr)
    println("maxArea : $result")
}
```

## Expected Output

```ruby
maxArea : 49
```