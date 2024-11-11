# Counting Element
## Overview
```ruby
fun countElements(strs:Array<String>){
    val countMap = mutableMapOf<String,Int>()
    for(str in strs){
        countMap[str] = countMap.getOrDefault(str,0)+1
    }
    for((key,value) in countMap){
        println("$key occurs $value times")
    }
}
```
```ruby
fun main() {
    val strs = arrayOf("apple", "banana", "apple", "orange", "banana", "apple")
    countElements(strs)
}
```

# Output
```ruby
apple occurs 3 times
banana occurs 2 times
orange occurs 1 times
```