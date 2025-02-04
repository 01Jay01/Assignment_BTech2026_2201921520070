"Explanation here..." 

Class Definition and Data Members -:
The class contains a list bookings to store booked time intervals.
The constructor MyCalendarTwo() initializes the list.

Booking Functionality (book method)-:
The book(int startTime, int endTime) method is responsible for adding a new booking while ensuring that no time slot is booked more than twice.
The method iterates through the bookings list to check if the new booking would cause a triple booking.
If an overlap is found between an existing booking and the new booking, the overlapping segment is passed to the check function to verify if this results in a third overlapping booking.
If the check function returns true, the booking is rejected.
Otherwise, the new interval is added to the bookings list.

Triple Booking Verification (check method)-:
The check(int start, int end) method checks whether a given time interval [start, end] overlaps with at least two existing intervals, leading to a triple booking.
It iterates through bookings, counting the number of overlapping intervals.
If the overlap count reaches 2, it means the booking would create a triple booking, and the function returns true.
Otherwise, it returns false, indicating that the booking is valid.

Time Complexity Analysis-:
book method:
The worst-case scenario occurs when all existing bookings overlap.
The function iterates through all N existing bookings to check for overlapping intervals.
The check function also iterates through the N bookings again, leading to O(N²) complexity in the worst case.
Thus, the time complexity of the book method is O(N²).

Space Complexity Analysis-:
The bookings list stores up to N booked intervals.
Each interval takes O(1) space.
The worst-case space complexity is O(N), where N is the number of bookings made.

