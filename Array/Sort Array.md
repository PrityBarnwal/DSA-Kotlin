# Sort Array

## Overview
To sort an array using logic, you can implement a sorting algorithm manually. 
There are various sorting algorithms, each with different characteristics and performance trade-offs.
 Here, I'll provide implementations for three popular sorting algorithms: 
 **Bubble Sort, Selection Sort, and Quick Sort.**


## Bubble Sort

Bubble Sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. 
The pass through the list is repeated until the list is sorted.

## Function and Implementation

```ruby
fun bubbleSortArray(arr:IntArray){
	var n = arr.size
 
	for(i in 0 until n-1){
		for(j in 0 until n-i-1){
			if(arr[j] > arr[j+1]){
			 val temp = arr[j]
                arr[j]=arr[j+1]
                arr[j+1]= temp
       
			}
		}
	}
}
```

```ruby

 fun main() {
    val arr = intArrayOf(3,2,4,1,7)
    bubbleSortArray(arr)
  
   println("Sorted array: ${arr.joinToString(", ")}")
 }

```

## Expected Output
[1,2,3,4,7]