# Two Sum

## OverView

   	In arrayList it which two value sum equal to target value

## Function and Implementation

```ruby
	fun twoSum(nums:IntArray,target:Int):IntArray{
		for(i in nums.indices){
			for(j in i+1 until nums.size -1){
				if(nums[i]+nums[j] == target){
				 return intArrayOf(i,j) 			// give position

				// return intArrayOf(nums[i],nums[j]) // give value
				}
			}
		}
		throw IllegalArgumentException("No Sum Found")
	}
```

```ruby
	fun main(){
		val arr = intArrayOf(2,3,5,7,8)
    	val target = 12
   		val result = twoSum(arr,target)
    	println(result.joinToString(","))
	}
```

## Expected Output

```ruby
	2,3   //position
	5,7   //sum of
```