# Merge Array

## OverView

   	Merge two array in a list

## Function and Implementation
```ruby
fun main(){
    val arr1 = intArrayOf(1,3,4,5)
    val arr2 = intArrayOf(3,4,5,6,6)
    val list = mergeArray(arr1,arr2)
    print(list.joinToString(","))
}
```
```ruby
fun mergeArray(arr1:IntArray,arr2:IntArray):IntArray{
    var result = mutableListOf<Int>()
    
    for(i in arr1){
        result.add(i)
    }
     for(i in arr2){
        result.add(i)
    }
     return result.toIntArray()
    
}
```

## Expected Output

```ruby
1,3,4,5,3,4,5,6,6
```