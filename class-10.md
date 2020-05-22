# Reading Notes 10  
To turn in your reading “Reply” to this discussion by teaching something that you learned. Then review what one of your classmates learned, and leave a comment.

Some ideas for how you might want to teach:

Use an analogy
Explain a detail in depth
Use WHY, WHAT, HOW structure
Tutorial / walk through an example
Write a quiz
Create a vocabulary/definition list
Write a cheat sheet
Create a diagram / visualization / cartoon of a topic
Anthropomorphize the concepts, and write a conversation between them
Build a map of the information
Construct a fill-in-the-blank worksheet for the topic

## Additional Resources  
* [Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)  

## Stacks and Queues  
### What is a Stack?  
- A stack is a datastructure that consists of `Nodes`. Each `Node` references the next Node in the stack, but does not reference its previous.  

#### Common Terminology for a stack is:  
- Push - Nodes or items that are put into the stacked are pushed  
    - Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in a stack.  
- Pop - Nodes or items that re removed from the stack are popped off.  
    - Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
- Top - This is the top of the stack.  
- Peek - When you `peek` you will view the value of the top Node in the stack.  
    - When conducting a peek, you will be inspecting the top Node of the stack.
- isEmpty - returns true when stack is empty otherwise returns false.  
    - If the input == None the output = Boolean. Another O(1) operation.  
- FILO - First In Last Out  
    - This means that the first item added in the stack will be the last item popped out of the stack.  
- LIFO - Last In First Out  
    - This means the last item added to the stack will be the first item popped out of the stack.  
- NOTE: Typically you will call `isEmpty` before you pop and or peek, as if you attempt to do either of those operations on an empty list an exception is raised. You can use a `try and catch` to avoid this.  

#### Common Terminology for a queue is:  
- Enqueue - Nodes or items that are added to the queue  
    - When you add an item to a queue, you use the `enqueue` action. This is an O(1) operation because it does not matter how many other items live in the queue (n).  
- Dequeue - Nodes or items that are removed from the queue.
    - If called when the queue is empty an exception is raised.  
    - When you remove an item from a queue, you use the `dequeue` action. This is an O(1) operation because it does not matter how many other items are in the queue. You are always just removing the `front` Node of the queue.
- Front - This is the front/first Node of the queue.  
- Rear - This is the rear/last Node of the queue.  
- Peek - When you peek you will view the value of the front Node in the queue. 
    - When conducting a peek, you will be inspecting the front Node of the queue.
    - If called when the queue is empty an exception will be raised.  
- isEmpty - returns true when queue is empty otherwise returns false.  
- FIFO - First In First Out  
    - This means that the first item in the queue will be the first item out of the queue.  
- LILO - Last In Last Out  
    - This means that the last item in the queue will be the last item out of the queue.  
