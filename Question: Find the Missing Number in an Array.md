# Question: Find the Missing Number in an Array

**Problem Description:**
You are given an array of integers from 1 to n with one number missing. Write a Java function to find the missing number.

**Solution:**

```java
public class MissingNumber {
    // Function to find the missing number in an array
    static int findMissingNumber(int[] nums) {
        int n = nums.length + 1;
        int expectedSum = n * (n + 1) / 2;
        int actualSum = 0;

        for (int num : nums) {
            actualSum += num;
        }

        return expectedSum - actualSum;
    }

    public static void main(String[] args) {
        // Example: Missing number in the array [1, 2, 4, 6, 3, 7, 8] is 5
        int[] nums = {1, 2, 4, 6, 3, 7, 8};

        int missingNumber = findMissingNumber(nums);

        System.out.println("Missing Number: " + missingNumber);
    }
}
```

**Explanation:**
The `findMissingNumber` function uses the concept of the sum of the first n natural numbers. It calculates the expected sum for the range [1, n+1], subtracts the actual sum of the given array, and returns the missing number.

This question assesses the candidate's ability to understand mathematical concepts and solve problems using basic arithmetic operations. It also tests their understanding of arrays and loops.
