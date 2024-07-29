# Find Maximum Element 
## Overview
In array list find which is the maximum element

# Functionality and implementation

```ruby
 fun findmax(s:Array<Int>):Int{
	var maxElemrnt = arr[0]
	for(i in 1 until s.size){
	if(arr[i]<maxElemrnt){
	maxElemrnt =arr[i]
 	}
 }
 	return maxElemrnt
}
```

Main Function and Example usage

```ruby
fun main(){
	var arr = arrayOf(1,2,3,4,6,7)
	val maxElementInArray = findmax(arr)
	printlin("maxElementInArray $maxElementInArray")
}
```

# Expected Output
```
 7
```