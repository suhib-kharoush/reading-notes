# Stacks and Queues:
- A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

- Common terminology for a stack is:
1. Push - Nodes or items that are put into the stack are pushed.
2. Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
3. Top - This is the top of the stack.
4. Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
5. IsEmpty - returns true when stack is empty otherwise returns false.

- Stacks follow these concepts:
- FILO: First In Last Out.

- Stack Visualization:
- Here’s an example of what a stack looks like. As you can see, the topmost item is denoted as the top. When you push something to the stack, it becomes the new top. When you pop something from the stack, you pop the current top and set the next top as top.next
- ![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

- Push O(1):
- Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

- Let’s walk through the steps:
1. First, you should have the Node that you want to add. Here is an example of a Node that we want to add to the stack.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack1.PNG)

2. Next, you need to assign the next property of Node 5 to reference the same Node that top is referencing: Node 4
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack2.PNG)

3. Technically at this point, your new Node is added to your stack, but there is no indication that it is the first Node in the stack. To make this happen, you have to re-assign our reference top to the newly added Node, Node 5.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack3.PNG)

- Pop O(1):
- Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack1.PNG)

1. The first step of removing Node 5 from the stack is to create a reference named temp that points to the same Node that top points to.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack2.PNG)

2. Once you have created the new reference type, you now need to re-assign top to the value that the next property is referencing. In our visual, we can see that the next property is pointing to Node 4. We will re-assign top to be Node 4.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack3.PNG)

3. We can now remove Node 5 safely without it affecting the rest of the stack. Before we do that though you may want to make sure that you clear out the next property in your current temp reference. This will ensure that no further references to Node 4 are floating around the heap. This will allow our garbage collector to cleanly and safely dispose of the Nodes correctly.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack4.PNG)

- Peek O(1):
- When conducting a peek, you will only be inspecting the top Node of the stack.
