"Explanation here..." 
Class Components and Explanation-:

Instance Variable (list):
The class maintains a list (list) that stores already booked intervals as an array of two integers: [startTime, endTime].

Constructor (MyCalendar):
Initializes list as an ArrayList<int[]> to store booking intervals.

Method: book(int startTime, int endTime):
This method attempts to book an event in the calendar.
It iterates through the list of existing bookings and checks if the new interval [startTime, endTime] overlaps with any existing booking.
If an overlap is found, it calculates the overlapping section (newStart and newEnd) and calls the check method.
The check method ensures there are no existing overlapping intervals.
If no conflicting bookings are found, the new interval is added to the list and returns true, indicating a successful booking.
If a conflict is detected, it returns false, rejecting the booking.

Method: check(int start, int end):
This method checks whether an overlapping interval already exists in list.
It iterates through all booked intervals and counts overlaps.
If at least one overlap (overlapCount == 1) is found, it returns true (indicating a conflict).
Otherwise, it returns false.

Time Complexity Analysis-:
book() Method:
The method iterates over all stored intervals, making its worst-case time complexity O(N) (where N is the number of booked intervals).
The additional call to check() also iterates through the list, contributing another O(N) operation.
Therefore, the total time complexity is O(N²) in the worst case.
check() Method:
This method iterates over all bookings, leading to a complexity of O(N).

Space Complexity Analysis-:
The list stores booked intervals, which requires O(N) space in the worst case.
No additional data structures are used apart from a few integer variables, so the overall space complexity remains O(N).
