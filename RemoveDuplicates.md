```ruby
fun main() {
    val kotlin =intArrayOf(2,4,5,8,9,4,2)
    println(removeDuplicate(kotlin).toList()) 
}

fun removeDuplicate(nums:IntArray):IntArray{
  val result = mutableListOf<Int>()
  
  for(num in nums){
      if(num !in result){
          result.add(num)
      }
  }
  return result.toIntArray()
}
```

