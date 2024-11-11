# Generate Parentheses
## Overview

```ruby
fun generateParaenthese(n:Int):List<String>{
    val result = mutableListOf<String>()
    fun backtrack(current:String,openCount:Int,closeCount:Int){
        if(current.length == 2*n){
            result.add(current)
            return
        }
        if (openCount < n) {
            backtrack(current + "(", openCount + 1, closeCount)
        }

        if (closeCount < openCount) {
            backtrack(current + ")", openCount, closeCount + 1)
        }
    }
      backtrack("", 0, 0)
    return result
}
```
```ruby
fun main() {
    val n = 3 // Example: Generate 3 pairs of parentheses
    val result = generateParentheses(n)
    println(result) // Prints: ["((()))", "(()())", "(())()", "()(())", "()()()"]
}
```

## Output
```ruby
[((())), (()()), (())(), ()(()), ()()()]
```