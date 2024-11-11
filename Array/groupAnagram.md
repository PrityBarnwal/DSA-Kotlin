# Group Anagram
## Overview

```ruby
fun grpAnagrams(strs:Array<String>):List<List<String>>{
    val map = mutableMapOf<String,MutableList<String>>()
    // Sort the string and use it as the key
    for(str in strs){
        val sortedStr = str.toCharArray().sorted().joinToString("")
     // Group anagrams together by adding them to the corresponding list in the map
        if(!map.containsKey(sortedStr)){
            map[sortedStr] = mutableListOf()
        }
        map[sortedStr]?.add(str)
    }
    return map.values.toList()
}
```
```ruby
fun main() {
    val strs = arrayOf("eat", "tea", "tan", "ate", "nat", "bat")
    val result = grpAnagrams(strs)
    println(result)
}
```
# Output
```ruby
[[eat, tea, ate], [tan, nat], [bat]]
```