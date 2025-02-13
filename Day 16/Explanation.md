"Explanation here..." 
The DetectSquares class is designed to efficiently track points on a 2D plane and count the number of axis-aligned squares that can be formed with a given point as one of the vertices.

1. Data Structures Used
List<int[]> coordinates: Stores all added points.
Map<String, Integer> counts: Maps each point (represented as a string "x@y") to the number of times it has been added. This helps in quickly retrieving counts of specific points when checking for squares.

2. Methods
Constructor:Initializes an empty list and hash map.
add(int[] point):Adds a new point to coordinates.
Updates the frequency count of this point in counts.
count(int[] point):Iterates through all stored points (coordinates).
For each point (x, y), checks if it can form a diagonal of a square with (px, py). This requires:
The x-coordinates or y-coordinates should not be the same.
The absolute difference between x-coordinates must be equal to the absolute difference between y-coordinates.
If a valid diagonal point is found, it calculates the number of squares by multiplying the count of the two missing corners:
(x, py) (top or bottom corner)
(px, y) (left or right corner)
Returns the total count of squares.

Time and Space Complexity
Time Complexity
add(int[] point):
Storing a point in coordinates → 
O(1).
Updating counts map → 
O(1).
Overall: 
O(1).
count(int[] point):
Iterates through all stored points → 
O(N), where N is the number of points in coordinates.
For each point, it retrieves two values from counts (both 
O(1)).
Overall: 
O(N).
Space Complexity
coordinates stores all points → 
O(N).
counts stores unique points with their frequencies → 
O(U), where U is the number of unique points.
Overall: 
O(N+U).



