"Explanation here..." 

Class Members-:
list: A List<Integer> that stores cumulative products.
prev: An integer variable that keeps track of the cumulative product.

Constructor-:
The constructor initializes:
list as an ArrayList and adds 1 as the first element.
prev is set to 1 to act as an identity value for multiplication.

add(int num) Method-:
If num is zero or negative, it resets list and prev because any number after a zero won't contribute to prior cumulative products.
Otherwise, it updates prev by multiplying it with num and appends prev to list.

getProduct(int k) Method-:
Retrieves the product of the last k elements.
The size of the list is n.
If k < n, it calculates the product as prev / list.get(n - 1 - k). This works because the list maintains cumulative products.
If k >= n, it means there was a reset due to zero, so it returns 0.

Time Complexity-:
add(int num):
In the worst case (reset scenario), it takes O(1) because clearing and reinitializing the list takes constant time.
Otherwise, appending a value to the list takes O(1).
Overall, O(1).

getProduct(int k):
The product retrieval only involves accessing two elements in the list and performing division.
Accessing an index in an ArrayList is O(1).
Overall, O(1).

Space Complexity-:
The space required for list is O(N), where N is the number of elements added since the last reset (after zero appears).
The integer variable prev takes O(1) space.
Overall, O(N).
