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
# Explaination
```ruby
1. For the first string "eat":
sortedStr = "aet"
The map is updated:
map = { "aet" -> ["eat"] }

2. For the second string "tea":
sortedStr = "aet"
Since "aet" already exists in the map, "tea" is added to the list:
map = { "aet" -> ["eat", "tea"] }

3. For the third string "tan":
sortedStr = "ant"
The map is updated:
map = { "aet" -> ["eat", "tea"], "ant" -> ["tan"] }

4. For the fourth string "ate":
sortedStr = "aet"
"ate" is added to the list for the key "aet":
map = { "aet" -> ["eat", "tea", "ate"], "ant" -> ["tan"] }

5. For the fifth string "nat":
sortedStr = "ant"
"nat" is added to the list for the key "ant":
map = { "aet" -> ["eat", "tea", "ate"], "ant" -> ["tan", "nat"] }

6. For the sixth string "bat":
sortedStr = "abt"
The map is updated:
map = { "aet" -> ["eat", "tea", "ate"], "ant" -> ["tan", "nat"], "abt" -> ["bat"] }

```
