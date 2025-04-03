# Search Rotated Array
## Function and Implementation

```ruby
fun searchRotatedArray(nums:IntArray,target:Int):Int{
    var left =0
    var right = nums.size-1
    while(left<=right){
        var mid = left + (right-left)/2
        if(nums[mid]==target) return mid
        if(nums[left] <= nums[mid]){
            if(target in nums[left]..nums[mid]){
                right =mid-1
            }else{
                left =mid+1
            }
        }else{
            if(target in nums[mid]..nums[right]){
                left = mid+1
            }else{
                right = mid-1
            }
        }
    }
    return -1
}
```
```ruby
fun main() {
    val nums = intArrayOf(4, 5, 6, 7, 0, 1, 2)
    val target = 0
    val result = searchRotatedArray(nums, target)
    println("Index of $target: $result")
}
```
## Output
```ruby
Index of 0: 4
```