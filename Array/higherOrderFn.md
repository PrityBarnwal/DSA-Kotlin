# Higher Order Function
## OverView

```ruby
fun <T> List<T>.customFilter(predicate: (T) -> Boolean): List<T> {
    val result = mutableListOf<T>()
    for (item in this) {
        if (predicate(item)) result.add(item)
    }
    return result
}
```
```ruby
fun main() {
    val numbers = listOf(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

    // Define a predicate function to filter even numbers
    val evenNumbers = numbers.customFilter { it % 2 == 0 }

    println("Even numbers: $evenNumbers")
}
```

Output
```ruby
Even numbers: [2, 4, 6, 8, 10]
```