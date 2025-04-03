```ruby
fun main() {
    val kotlin = intArrayOf(1, 3,4, 5, 7,8) 
    println(kotlin.evenOdd().toList()) 
}

fun IntArray.evenOdd(): IntArray {
    val evenNumbers = this.filter { it % 2 == 0 }.toIntArray()
    
    if (evenNumbers.isNotEmpty()) {
        println("even")
    } else {
        println("odd")
    }
    
    return evenNumbers
}
```

# Output
even
[4, 8]
