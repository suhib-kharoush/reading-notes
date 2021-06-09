# Linked Lists:

- What is a Linked List?
- A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

- Terminology:
- - Linked List - A data structure that contains nodes that links/points to the next node in the list.
- - Singly - Singly refers to the number of references the node has. A Singly linked list
- - Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
- - Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
- - Next - Each node contains a property called Next. This property contains the reference to the next node.
- - Head - The Head is a reference of type Node to the first node in a linked list.
- - Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

- What does it look like?
- ![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)

- Adding a Node:
- Adding O(1)
- Order of operations is extremely important when it comes to working with a Linked List. What I mean by this is you must be careful that all references to each link/node is properly assigned.


# Information is all around us:

- In the world of software, the ways that we choose to organize our information is half the battle.

- Regardless of which language we start coding in, one of the first things that we encounter are data structures, which are the different ways that we can organize our data; variables, arrays, hashes, and objects are all types of data structures. But these are still just the tip of the iceberg when it comes to data structures; there are a lot more, some of which start to sound super complicated the more that you hear about them.

- Linear data structures:
![](https://miro.medium.com/max/875/1*Xokk6XOjWyIGCBujkJsCzQ.jpeg)


- Big O Notation is a way of evaluating the performance of an algorithm.

- As far as linked lists go, however, the two types of Big O equations to remember are O(1) and O(n).


- ![](https://miro.medium.com/max/625/1*FC0XX0-9Vx7yCS0dTS2Zrw.jpeg)

- An O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
- An O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.