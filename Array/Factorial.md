# Implementation
```ruby

fun main(){
    println(factorial(5))
}

fun factorial(n:Int):Long{
    var result = 1L
    for(i in 2..n){
        result *= i
    }
    return result
}

```

