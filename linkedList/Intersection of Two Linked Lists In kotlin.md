#  Intersection of Two Linked Lists In kotlin

## Overview
This function leverages the property that two pointers traversing two lists will eventually meet at the intersection point if there is one. This is an efficient solution with O(N + M) time complexity, where N and M are the lengths of the two linked lists, and O(1) space complexity.

## Function and Implementation

data class ListNode(var value: Int, var next: ListNode? = null)                                   

```ruby
 fun getIntersectionNode(headA:ListNode?, headB:ListNode?):ListNode? {
        var a = headA
   		var b = headB
 	
   
    while (a != b) {
        println("Pointer A is at node with value: ${a?.value ?: "null"}")
        println("Pointer B is at node with value: ${b?.value ?: "null"}")
        
        a = if (a == null) headB else a.next
        b = if (b == null) headA else b.next
        
          println("After moving, Pointer A is at: ${a?.value ?: "null"}")
       	  println("After moving, Pointer B is at: ${b?.value ?: "null"}")
          println("----------------------------")
    }


    return a

    }
```

 ```ruby
fun main() {
  
 
    val headA = ListNode(3, ListNode(6, ListNode(9, ListNode(8,ListNode(10)))))
    val headB = ListNode(4, ListNode(7,  ListNode(2,ListNode(5,ListNode(8,ListNode(10))))))

  
    val intersectionNode = getIntersectionNode(headA, headB)

    if (intersectionNode != null) {
        println("Intersection at node with value: ${intersectionNode.value}")
    } else {
        println("No intersection")
    }
}

```r

## Expected Output: 
```ruby
8
 ```



##Print Section how it work
```ruby
Pointer A is at node with value: 3
Pointer B is at node with value: 4
After moving, Pointer A is at: 6
After moving, Pointer B is at: 7
----------------------------
Pointer A is at node with value: 6
Pointer B is at node with value: 7
After moving, Pointer A is at: 9
After moving, Pointer B is at: 2
----------------------------
Pointer A is at node with value: 9
Pointer B is at node with value: 2
After moving, Pointer A is at: 8
After moving, Pointer B is at: 5
----------------------------
Pointer A is at node with value: 8
Pointer B is at node with value: 5
After moving, Pointer A is at: 10
After moving, Pointer B is at: 8
----------------------------
Pointer A is at node with value: 10
Pointer B is at node with value: 8
After moving, Pointer A is at: null
After moving, Pointer B is at: 10
----------------------------
Pointer A is at node with value: null
Pointer B is at node with value: 10
After moving, Pointer A is at: 4
After moving, Pointer B is at: null
----------------------------
Pointer A is at node with value: 4
Pointer B is at node with value: null
After moving, Pointer A is at: 7
After moving, Pointer B is at: 3
----------------------------
Pointer A is at node with value: 7
Pointer B is at node with value: 3
After moving, Pointer A is at: 2
After moving, Pointer B is at: 6
----------------------------
Pointer A is at node with value: 2
Pointer B is at node with value: 6
After moving, Pointer A is at: 5
After moving, Pointer B is at: 9
----------------------------
Pointer A is at node with value: 5
Pointer B is at node with value: 9
After moving, Pointer A is at: 8
After moving, Pointer B is at: 8
----------------------------
Intersection at node with value: 8
```