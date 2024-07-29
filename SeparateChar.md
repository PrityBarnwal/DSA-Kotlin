# Separating Characters in a String with Kotlin

## overview

- This Kotlin function separates a given string into three categories: alphabets, digits, and special characters. The result is returned as a Triple containing these three categories.

## Function Implementation
```ruby
fun separetChar(input:String):Triple<String,String,String>{
    val alphabet =input.filter{it.isLetter()}
    val number =input.filter{it.isDigit()}
    val special = input.filter{!it.isLetterOrDigit()}
    return Triple(alphabet,number,special)
}
```

## Main Function and Example Usage
```ruby
fun main() {
    val s= "abcdef@&90"
    val saparte = separetChar(s)
    println("Hello, world$saparte")
}
```
## Expected Output

```ruby
 Hello, world (abcdef, 90, @&)
 ```