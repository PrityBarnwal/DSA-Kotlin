# Rotate largest and smallest index
## Overview
```ruby
fun main(){
    val s = arrayOf(3,7,1,6,9)
    val maxIndex = s.indexOf(s.maxOrNull())
    val minIndex = s.indexOf(s.minOrNull())
    if(s[maxIndex] != -1 && s[minIndex] != -1){
        val temp = s[maxIndex]
        s[maxIndex] =s[minIndex]
        s[minIndex] = temp
    }
    println(s.joinToString(","))
}
```