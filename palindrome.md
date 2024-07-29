# Palindrome 
## Overview
 on reverse of string from left and right side reading is same 

## Functionality Implementation

```ruby 
fun palindrome(s:String):Boolean{
    var a =0 
    var b = s.length -1
    while(a < b){
        if(s[a]!=s[b]){
           return false
        }
        a++
        b--
    }
    return true
}
```

## Main Function and Example Usage

```ruby
fun main() {
   
    val palindromeInput ="abba"
    val isPalindrome = palindrome(palindromeInput)
    println("palindrom $isPalindrome")
    }
```

## Expected Output

```ruby
palindrom true
```