```ruby
fun main() {
    val kotlin ="abba"
    println(palindrome(kotlin)) 
}

fun palindrome(nums:String):Boolean{
  var left = 0
    var right = nums.length -1
    while(left < right){
        if(nums[left] != nums[right]){
            return false
        }
        left++
        right--
    }
    return true
}
```

