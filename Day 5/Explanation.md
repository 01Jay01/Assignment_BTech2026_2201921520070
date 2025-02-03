"Explanation here..." 
Class Explanation-:

Instance Variables:
int ptr: A pointer (ptr) that keeps track of the current smallest index from where we can start returning values.
String[] res: An array of strings (res) to store the stream values. The size of this array is n, which is passed as an argument to the constructor.

Constructor (OrderedStream(int n)):
Initializes ptr to 0 (beginning of the stream).
Allocates memory for the res array of size n.

Method: insert(int idKey, String value) -> List<String>:
Inserts value at index idKey - 1 in the res array. This is because the input index is 1-based, but Java arrays use 0-based indexing.
A List<String> (list) is created to store contiguous values that can be returned.
If ptr points to a non-null element, it means that contiguous elements are available, and we start adding elements to the list while incrementing ptr.
The method returns the list containing elements in order.

Time Complexity-:
Insertion is O(1), as it directly assigns a value in the array.
The while loop runs at most n times in total across all insertions.
Across n calls, each element is processed once in a single pass, making the amortized complexity O(1) per call.

Space Complexity-:
The array res of size n is maintained, leading to a space complexity of O(n).
