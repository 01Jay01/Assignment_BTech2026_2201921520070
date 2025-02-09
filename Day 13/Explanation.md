"Explanation here..." 
Intuition-:
The goal of the RecentCounter class is to count the number of requests that occurred in the last 3000 milliseconds (ms). Each time a request is made (using the ping method), we record the time and maintain a count of all requests within the last 3000 ms. By efficiently tracking only the relevant requests, we can quickly compute the result.

Approach-"
Data Structure: Use an array records to store timestamps of requests. The start and end indices mark the window of valid requests within the last 3000 ms.
ping(int t) Method:
Add Timestamp: Insert the current timestamp t at the position indicated by end.
Remove Outdated Requests: Increment the start index until the requests are within the 3000 ms window (t - records[start] <= 3000).
Count Valid Requests: Return the count of requests within the window (end - start), which represents the number of valid requests in the last 3000 ms.

Complexity-:
Time complexity: O(n)

Space complexity: O(1)
