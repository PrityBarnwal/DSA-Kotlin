```ruby
fun main() {
 val input = listOf(2, 3, 2, 4, 3, 5)
 val map = mutableMapOf<Int, Int>()
    for (i in input){
       map[i] = map.getOrDefault(i, 0) + 1  
    }
   
    val result = input.firstOrNull { map[it] == 1 }
	println(result) 
}
```
```ruby
# Output
4
```