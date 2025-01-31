"Explanation here..." 

MyStack constructor:
Initialize a new instance of the MyStack class.
Create an empty deque named q to store the stack elements.

push Method:
Accept an integer x as input.
Append the input integer x to the right end of the deque q.
Loop for the number of times equal to the length of the deque minus one (length - 1).
In each iteration, remove an element from the left end of the deque (popleft) and immediately append it back to the right end.
This loop ensures that the last added element is at the front of the deque, simulating the behavior of a stack.

pop Method:
Remove and return the element from the left end of the deque q.
This operation effectively mimics the behavior of popping an element off the stack.

top Method:
Return the element at the left end of the deque q without removing it.
This operation provides the top element of the stack without altering the stack itself.

empty Method:
Check if the length of the deque q is equal to 0.
If the length is 0, the stack is empty, so return True; otherwise, return False.

Complexity
Time complexity:
pop, top and empty are O(1), push is O(n)
Space complexity: O(n)
