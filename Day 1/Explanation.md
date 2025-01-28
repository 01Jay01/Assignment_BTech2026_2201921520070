 "Explanation for day 1 here..." 
 The ParkingSystem class is a simple program to manage parking spaces for three types of cars: big, medium, and small. It keeps track of the available parking spaces for each type using three integer variables: big, medium, and small.

The class has two main components:

Constructor: Initializes the parking system with the number of available spaces for each car type.
addCar Method: Checks if a car of a specific type (big, medium, or small) can be parked.
If a parking space for the given car type is available, it decreases the corresponding space count by 1 and returns true (indicating the car is successfully parked).
If no space is available for the car type, it returns false (indicating the car cannot be parked).
Each car type is represented by a number:

1 for big cars
2 for medium cars
3 for small cars
Example:
If the system starts with 1 big, 1 medium, and 0 small spaces:

Adding a big car returns true and reduces big spaces to 0.
Adding another big car returns false as no big spaces remain.
Adding a medium car returns true.
Adding a small car returns false as no small spaces were available initially.
This program helps track parking availability efficiently.
