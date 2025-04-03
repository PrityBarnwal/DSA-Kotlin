```ruby
fun main() {
    val s= "abcdef@&90A"
    val saparte = separetChar(s)
    println("Hello, world$saparte")
}
fun separetChar(input:String):Triple<String,String,String>{
    var alphabet =""
    var number =""
    var special = ""
    for(char in input){
        when{
            (char in 'a'..'z'|| char in 'A'..'Z') -> alphabet += char
            (char in '0'..'9') -> number +=char
            else -> special +=char
        }
    }
    return Triple(alphabet,number,special)
}
```

