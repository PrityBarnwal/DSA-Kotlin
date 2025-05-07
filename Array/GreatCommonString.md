# Implementation
```ruby

    fun gcdOfStrings(str1: String, str2: String): String {
        if((str1+str2) != (str2+str1)) return ""
        val gcdLength = str1.length.gcd(str2.length)
        return str1.substring(0,gcdLength)
    }

    fun Int.gcd(other:Int):Int{
        var a =this
        var b = other
        while(b !=0){
            val temp =b
            b = a % b
            a = temp
        }
        return a
    }

```

```ruby
fun main(){
    val word1 ="ABAB"
     val word2 ="ABCD"
     val result = gcdOfStrings(word1,word2)
     println(result)
}

```
# Input 
 word1 = "ABAB", word2 = "ABCD"
# Output
"AB"
```
