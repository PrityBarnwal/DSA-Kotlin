# Reverse LinkedList

## Overview
A linked list consists of a data element known as a node. 
And each node consists of two fields: one field has data, 
and in the second field, the node has an address that keeps a reference to the next node


## Function and Implementation

import java.util.LinkedList
```ruby

data class Node(
var value:Int, var next: Node? = null )

fun reversedLinkedList(head:Node?):Node?{
	var current = head
	var previous : Node? = null
	var next : Node? = null

	while(current != null){
	next = current.next
	current.next = previous
	previous = current 
	current = next
	}
	return previous
}

fun main(){
	val head = Node(1,Node(2,Node(3,Node(4))))

	val reversedHead = reversedLinkedList(head)

	var current = reversedHead
	while(current != null){
	println("{current.value}")
	current = current.next
	}

}
```

## Expected Output
```ruby
[4,3,2,1]

```