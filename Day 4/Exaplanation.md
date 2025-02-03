"Explanation here..." 
Class Components and Methods:

Instance Variables:
private Random random; → This instance of the Random class is used to generate random numbers.
int[] arr=new int[50]; → This integer array holds the original values of the input array.

Constructor (Solution(int[] nums)):
This constructor initializes the array arr using the input nums.
The random instance is created using new Random() to generate random numbers.
However, there is a bug in the constructor: arr is first initialized to a size of 50, but it is later reassigned to nums. Instead of this.arr = nums, it should be this.arr = Arrays.copyOf(nums, nums.length); to ensure that the original array is not modified.

Method: reset()
This method returns the original array arr, restoring it to its initial configuration.
Time Complexity: O(1) since it simply returns a reference to the original array.
Space Complexity: O(1) as no additional space is used.

Method: shuffle()
This method returns a randomly shuffled version of the array using the Fisher-Yates Shuffle Algorithm:
A new array shuffled[] is created as a copy of arr using Arrays.copyOfRange(arr, 0, arr.length).
It iterates through the array in reverse order.
In each iteration, it selects a random index j in the range [0, i].
The values at indices i and j are swapped to ensure randomness.

Time Complexity: O(n) because it iterates through the entire array once, making a constant-time swap operation per iteration.
Space Complexity: O(n) due to the additional shuffled array that stores the modified version.
