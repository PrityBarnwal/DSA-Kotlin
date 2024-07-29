# Find Minimum Element 
## Overview
In array list find which is the minimum element
## Functionality and implementation
```ruby
 fun findmax(s:Array<Int>):Int{
 if(arr.isEmpty()){
        throw IllegalArgumentException("Array is Empty")
    }

	var minElemrnt = arr[0]
	for(i in 1 until s.size){
	if(arr[i] > minElemrnt){
	minElemrnt =arr[i]
 	}
 }
 	return minElemrnt
}
```
## Main Function and Example usage

```ruby
fun main(){
	var arr = arrayOf(1,2,3,4,6,7)
	val minElementInArray = findmax(arr)
	printlin("minElementInArray $minElementInArray")
}
```

## Expected Output

 ```
 1
 ```