# Find the Nth Node from End of LinkedList

## Overview
A linked list consists of a data element known as a node. 
And each node consists of two fields: one field has data, 
and in the second field, the node has an address that keeps a reference to the next node


## Function and Implementation


data class Node(val value: Int, var next: Node? = null)

```ruby

fun findNthFromEnd(head: Node?, n: Int): Node? {
    var firstPointer = head
    var secondPointer = head

    // Move firstPointer n steps ahead
    for (i in 0 until n) {
        firstPointer = firstPointer?.next
    }

    // Move both pointers until firstPointer reaches the end
    while (firstPointer != null) {
        firstPointer = firstPointer.next
        secondPointer = secondPointer?.next
    }

    // secondPointer now points to the Nth node from the end
    return secondPointer
}
```

```ruby
fun main() {
    val head = Node(1,Node(2,Node(3,Node(4,Node(5)))))
   

    val n = 2
    val nthNode = findNthFromEnd(head,n)

    if (nthNode != null) {
        println("The $n-th node from the end has the value: ${nthNode.value}")
    } else {
        println("The list is shorter than $n nodes.")
    }
}
```

## Expected Output: 
```ruby
The 2-th node from the end has the value: 4
```