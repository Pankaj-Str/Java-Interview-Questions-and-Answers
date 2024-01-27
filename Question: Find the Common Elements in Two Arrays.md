# Question: Find the Common Elements in Two Arrays

**Problem Description:**
Given two arrays of integers, write a Java function to find and print the common elements present in both arrays.

**Solution:**

```java
import java.util.HashSet;

public class CommonElementsInArrays {
    // Function to find common elements in two arrays
    static void findCommonElements(int[] arr1, int[] arr2) {
        HashSet<Integer> set = new HashSet<>();
        for (int num : arr1) {
            set.add(num);
        }

        System.out.print("Common elements: ");
        for (int num : arr2) {
            if (set.contains(num)) {
                System.out.print(num + " ");
            }
        }
    }

    public static void main(String[] args) {
        int[] arr1 = {1, 2, 4, 5, 6};
        int[] arr2 = {2, 3, 5, 7};

        System.out.println("Array 1: [1, 2, 4, 5, 6]");
        System.out.println("Array 2: [2, 3, 5, 7]");

        findCommonElements(arr1, arr2);
    }
}
```

**Explanation:**
This solution uses a HashSet to store unique elements from the first array (`arr1`). Then, it iterates through the second array (`arr2`) and checks if each element is present in the HashSet. If it is, the element is a common element, and it is printed.

This question assesses the candidate's knowledge of data structures (HashSet in this case) and their ability to efficiently solve problems involving arrays and sets.
