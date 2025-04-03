```ruby
fun main() {
    val kotlin = "Hello"
    println(reverseString(kotlin)) 
}

fun reverseString(s:String):String{
   var charAray = s.toCharArray()
    var left =0
    var right = s.length-1
    
    while(left < right){
       var temp = charAray[left]
        charAray[left] = charAray[right]
      	charAray[right]=temp
        left++
        right--
    }
    return String(charAray)
}
```

