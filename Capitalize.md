```ruby
fun main() {
    val kotlin ="hello world"
    println(kotlin.getLastCapital())
}
```
```ruby
fun String.getLastCapital():String{
    return this.split(" ").joinToString(" ") { it.replaceFirstChar{ch->
        ch.uppercase()
    }}
}
## Input 
"hello world"
## Output
"Hello World"
```
```ruby
fun String.getLastCapital():String{
    return this.dropLast(1) + this.last().uppercase()
}
## Input 
"hello world"
## Output
"Hello WorlD"
```


```ruby
fun String.getFirstCapital():String{
    return this.first().uppercase() + this.drop(1)
}
## Input 
"hello world"
## Output
"Hello WorlD"
```


```ruby
fun main() {
    val kotlin =intArrayOf(1,3,4,5,7)
    println(kotlin.max() - kotlin.min())
}

```