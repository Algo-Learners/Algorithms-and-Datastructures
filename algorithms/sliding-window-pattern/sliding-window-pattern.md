## Introduction to the sliding window pattern 

the sliding window pattern! It's a clever technique frequently used in algorithms to solve problems involving subarrays or substrings. The core idea is to maintain a "window" of elements within a larger data structure (like an array or string) and then slide this window across the data, performing some operation at each step.

This pattern really shines when you need to find things like:

    The maximum or minimum sum of a contiguous subarray of a fixed size.
    The longest or shortest substring containing a certain number of distinct characters.
    Checking if a string contains a permutation of another string.


The beauty of the sliding window approach lies in its efficiency. Instead of repeatedly iterating over all possible subarrays or substrings, you perform computations incrementally as the window slides, often reducing the time complexity significantly.


The sliding window pattern can be broadly categorized into two main types based on whether the size of the window remains constant or changes dynamically:


1. **Static (or Fixed-Size) Sliding Window**

In this type, the size of the window, often denoted as k, is fixed throughout the process. You initialize a window of size k, perform the required operation on the elements within this window, and then slide the window one element at a time to the right.

**When to use it:**

    When the problem involves processing contiguous subarrays or substrings of a specific, predetermined length.
    Finding the maximum/minimum sum of a subarray of size k.   

Calculating the average of all subarrays of size k.
Counting occurrences of a specific pattern (like an anagram) within a window of a fixed size.


**How it works (Conceptual Steps):**

    Initialize the window: Calculate the result for the first window of size k (from the beginning of the data structure).
    Slide the window: Iterate through the rest of the data structure. In each step:
        "Slide" the window by one position to the right. This means removing the element that went out of the left end of the window and adding the element that entered from the right end.
        Update the result based on the new window.
    Keep track of the desired value: Maintain a variable to store the maximum, minimum, count, or any other required value encountered during the sliding process.

**Example:** 

Find the maximum sum of any contiguous subarray of size 3 in the array [1, 4, 2, 10, 2, 3, 1, 0, 20].

    Initial window [1, 4, 2], sum = 7.
    Slide: [4, 2, 10], sum = 16.
    Slide: [2, 10, 2], sum = 14.
    
