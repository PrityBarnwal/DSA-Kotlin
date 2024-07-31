# Detect a Cycle in LinkedList in kotlin

## Overview
To detect a cycle in a linked list in Kotlin, you can use Floyd's Cycle-Finding Algorithm, 
also known as the Tortoise and Hare algorithm. This algorithm uses two pointers,
a slow pointer (tortoise) and a fast pointer (hare), which move at different speeds through the list. 
If there is a cycle, the fast pointer will eventually meet the slow pointer.

## Function and Implementation


data class Node(var value: Int, var next: Node? = null)
```ruby
fun hasCycle(head: Node?): Boolean {
    if (head == null) return false

    var slow: Node? = head
    var fast: Node? = head.next

    while (fast != null && fast.next != null) {
        if (slow == fast) return true
        slow = slow?.next
        fast = fast.next?.next
    }

    return false
}
```

```ruby
fun main() {
    // Create a list: 1 -> 2 -> 3 -> 4 -> 5
    
    val head = Node(1,Node(2,Node(3,Node(4,Node(5)))))
    
      // Introduce a cycle: 5 -> 3
     var node3 = head.next?.next
    var node5 = node3?.next?.next
    node5?.next = node3

    // Detect cycle
    println(hasCycle(head)) // Output: true
}
```

## Expected Output: 
```ruby
true
```