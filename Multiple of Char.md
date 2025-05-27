```ruby
fun main() {
    val input = listOf(2, 3, 2, 3, 4, 5)

    val map = mutableMapOf<Int, Int>()
    for (i in input) {
        map[i] = map.getOrDefault(i, 0) + i
    }
    println("$map")
}
}
```
```ruby
# Output
2=4, 3=6, 4=1, 5=1
```