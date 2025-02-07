"Explanation here..." 

Class Initialization (FindSumPairs Constructor)-:
The constructor takes two integer arrays, nums1 and nums2.
It initializes:
nums1 and nums2 to store the given arrays.
A HashMap<Integer, Integer> named hm, which maps each unique number in nums2 to its frequency.
The hm is populated by iterating over nums2 and counting occurrences of each number.
Time Complexity:Populating hm requires iterating over nums2 → O(N2) (where N2 is the size of nums2).
Space Complexity: O(N2) (for storing frequencies in the hashmap).

Updating nums2 (add Method)-:
The method add(int index, int val) modifies nums2 at the specified index by adding val to nums2[index].
Steps:
Retrieve the old value of nums2[index].
Update the frequency of the old value in hm:
If it was the only occurrence, remove it from hm.
Otherwise, decrement its count.
Update nums2[index] by adding val.
Add the new value to hm (increase its count or initialize it).
Time Complexity:HashMap operations (get, put, remove) are O(1) on average.
Thus, this method runs in O(1).
Space Complexity:The space remains O(N2) since we store nums2 frequencies.

Counting Pairs (count Method)-:
The method count(int tot) calculates how many pairs (nums1[i], nums2[j]) satisfy nums1[i] + nums2[j] == tot.
Steps:
Initialize count = 0.
Iterate through each number num in nums1.
Compute complement = tot - num.
If complement exists in hm, add its frequency to count.
Time Complexity:We iterate through nums1, and for each element, we perform a hashmap lookup O(1).
Thus, the total complexity is O(N1) (where N1 is the size of nums1).
Space Complexity:No additional space is used → O(1).