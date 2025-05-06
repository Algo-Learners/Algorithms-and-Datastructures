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
    

2. **Dynamic (or Variable-Size) Sliding Window**

In this type, the size of the window is not fixed and can expand or shrink based on certain conditions defined by the problem. You typically use two pointers, one to mark the beginning of the window and another to mark the end. These pointers move to adjust the window size to satisfy the given constraints.  

**When to use it:**

   [x] When the problem asks for a subarray or substring that meets a certain condition, but the size of this subarray/substring is not predetermined.

   [x] Finding the longest/shortest substring with a specific number of distinct characters.   
   [x] Finding the smallest window in a string containing all characters of another string.  
   [x] Finding subarrays with a sum equal to a target value.


**How it works (Conceptual Steps):**

    Initialize pointers: Set a start pointer (left end of the window) and an end pointer (right end of the window) both to the beginning of the data structure.
    Expand the window: Move the end pointer to the right, expanding the window, until a certain condition is met.   

    Shrink the window: Once the condition is met, move the start pointer to the right, shrinking the window, while the condition remains true. This helps in finding the optimal (e.g., smallest or longest) window that satisfies the condition.
    Repeat: Continue expanding and shrinking the window until the end pointer reaches the end of the data structure.
    Keep track of the desired value: Maintain a variable to store the best (e.g., maximum length, minimum length) result found so far.

Example: Find the length of the longest substring without repeating characters in the string "abcabcbb".

    start = 0, end = 0, window "", length = 0.
    end = 1, window "a", length = 1.
    end = 2, window "ab", length = 2.
    end = 3, window "abc", length = 3.
    end = 4, window "abca". Condition violated (repeating 'a'). Move start.
    start = 1, window "bca", length = 3.
