# Implementation
```ruby
fun mergeAlternately(word1: String, word2: String): String {
           val result = StringBuilder()
        val maxLength = maxOf(word1.length ,word2.length)

        for(i in 0 until maxLength){
            if(i < word1.length){
                result.append(word1[i])
            }
             if(i < word2.length){
                result.append(word2[i])
            }
        }
    return result.toString()
    }
```

``ruby
fun main(){
    val word1 ="abc"
     val word2 ="pqr"
     val result = mergeAlternately(word1,word2)
     println(result)
}

```
# Input 
 word1 = "abc", word2 = "pqr"
# Output
"apbqcr"
```
