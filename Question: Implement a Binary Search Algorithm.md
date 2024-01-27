# Question: Implement a Binary Search Algorithm 

**Problem Description:**
Write a Java function to perform a binary search on a sorted array and return the index of a given target element. If the target is not present, return -1.

**Solution:**

```java
public class BinarySearch {
    // Function to perform binary search on a sorted array
    static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2;

            if (arr[mid] == target) {
                return mid; // Target found, return the index
            } else if (arr[mid] < target) {
                left = mid + 1; // Target is in the right half
            } else {
                right = mid - 1; // Target is in the left half
            }
        }

        return -1; // Target not found
    }

    public static void main(String[] args) {
        int[] sortedArray = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        int target1 = 5;
        int target2 = 11;

        System.out.println("Sorted Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]");
        System.out.println("Searching for target " + target1 + ": Index " + binarySearch(sortedArray, target1));
        System.out.println("Searching for target " + target2 + ": Index " + binarySearch(sortedArray, target2));
    }
}
```

**Explanation:**
The `binarySearch` function performs a binary search on the sorted array. It maintains two pointers, `left` and `right`, and calculates the middle index (`mid`). It compares the element at the middle index with the target and narrows down the search space accordingly. This process continues until the target is found or the search space is empty.

This question assesses the candidate's understanding of binary search, a fundamental algorithm used for efficiently searching sorted data sets.
