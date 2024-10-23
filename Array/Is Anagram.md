# Is Anagram

## Overview

In array list find which is the maximum element

#### Functionality and implementation

    import java.util.Arrays
    fun main() {
        val string1 = "listen"
        val string2 = "silent"
        if (isAnagram(string1, string2)) {
        println("$string1 and $string2 are anagrams.")
    	} else {
        println("$string1 and $string2 are not anagrams.")
    	}
    }
        fun isAnagram(str1:String,str2:String): Boolean{
        if(str1.length != str2.length){
            return false
        }
        val charArray1 = str1.toCharArray()
        val charArray2 = str2.toCharArray()
        Arrays.sort(charArray1)
    	Arrays.sort(charArray2)
    
     	val sortedString1 = String(charArray1)
     	val sortedString2 = String(charArray2)
      	return sortedString1 == sortedString2
      }
