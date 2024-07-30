# LinkedList Sort Problems

## Overview
A linked list consists of a data element known as a node. 
And each node consists of two fields: one field has data, 
and in the second field, the node has an address that keeps a reference to the next node

## Related Questions

# Insert Start Item in LinkedList

## Function and Implementation

import java.util.LinkedList
```ruby
fun main(){
	val linkedList = LinkedList<Int>()
	linkedList.add(1)
	linkedList.add(2)
	linkedList.add(3)
	linkedList.add(4)
	linkedList.addFirst(6)
		// or linkedList.add(1,6)
	println(linkedList)
}
```

## Expected Output
```ruby
[6,1,2,3,4]
```

# Insert End Item in LinkedList

## Function and Implementation

import java.util.LinkedList
```ruby
fun main(){
	val linkedList = LinkedList<Int>()
	linkedList.add(1)
	linkedList.add(2)
	linkedList.add(3)
	linkedList.add(4)
	linkedList.addLast(6)
	// or linkedList.add(linkedList.size,6)
	println(linkedList)
}
```

## Expected Output
```ruby
[1,2,3,4,6]
```


# Delete Item in LinkedList

## Function and Implementation

import java.util.LinkedList
```ruby
fun main(){
	val linkedList = LinkedList<Int>()
	linkedList.add(1)
	linkedList.add(2)
	linkedList.add(3)
	linkedList.add(4)

	// remove item from 0th position
	 linkedList.remove(0)
    println("After removing the 0th position: $linkedList")
	
	// remove item from last position
	 linkedList.remove(linkedList.size -1)
  	  println("After removing the last position: $linkedList")

// remove item from middle position
	val mid = linkedList.size-1/2
	 linkedList.remove(mid)
    println("After removing the middle position: $linkedList")
	
}

```

## Expected Output
```ruby
After removing the 0th position === [2,3,4]

After removing the last position === [1,2,3]

After removing the middle position === [1,2,4]
```


# Find Length and search Element in LinkedList

## Function and Implementation

import java.util.LinkedList
```ruby
fun main(){
	val linkedList = LinkedList<Int>()
	linkedList.add(1)
	linkedList.add(2)
	linkedList.add(3)
	linkedList.add(4)

	//length 
	println("size === {linkedList.size}")

	var searchElement = 4
	if(linkedList.contains(searchElement)){
		println("found")
	}else{
		println("not found")
	}
}
```

## Expected Output
```ruby
size === 4
[found]
```