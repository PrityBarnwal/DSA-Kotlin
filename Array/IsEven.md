# Implementation
```ruby

fun main(){
val number = 6
    println(number.isEven()
}

fun Any.isEven():Boolean{
    return when(this){
        is Int -> this %2 ==0
        is String -> this.length % 2==0
        else -> false
    }
}

```

