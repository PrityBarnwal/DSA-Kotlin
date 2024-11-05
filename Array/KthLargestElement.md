# Kth Largest Element

## Overview
```ruby
fun sortDescenting(nums:IntArray){
    val n = nums.size
    for(i in 0 until n){
        for(j in 0 until n-1-i){
            if(nums[j] < nums[j+1]){
                val temp = nums[j]
                nums[j] = nums[j+1]
                nums[j+1] = temp
            }
        }
    }
}
```
```ruby
fun findKthLargest(nums: IntArray, k: Int): Int {
    sortDescenting(nums)  
    return nums[k - 1]
}
```
```ruby
fun main() {
    val array = intArrayOf(1,2,5,3,6,8,7)
    val k = 3
    println("kth largest Element : ${findKthLargest(array, k)}")
}
```
# Output
```ruby
kth largest Element : 6
```