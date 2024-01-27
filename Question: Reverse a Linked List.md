
## Question: Reverse a Linked List

**Problem Description:**
Write a Java function to reverse a singly linked list.

**Solution:**

```java
class Node {
    int data;
    Node next;

    Node(int data) {
        this.data = data;
        this.next = null;
    }
}

public class LinkedListReverse {
    // Function to reverse a linked list
    static Node reverseLinkedList(Node head) {
        Node prev = null;
        Node current = head;
        Node next = null;

        while (current != null) {
            next = current.next;
            current.next = prev;
            prev = current;
            current = next;
        }

        // The new head is the last node after reversal
        head = prev;
        return head;
    }

    // Function to print a linked list
    static void printLinkedList(Node head) {
        Node current = head;
        while (current != null) {
            System.out.print(current.data + " ");
            current = current.next;
        }
        System.out.println();
    }

    public static void main(String[] args) {
        // Create a sample linked list: 1 -> 2 -> 3 -> 4 -> 5
        Node head = new Node(1);
        head.next = new Node(2);
        head.next.next = new Node(3);
        head.next.next.next = new Node(4);
        head.next.next.next.next = new Node(5);

        System.out.println("Original Linked List:");
        printLinkedList(head);

        // Reverse the linked list
        head = reverseLinkedList(head);

        System.out.println("Reversed Linked List:");
        printLinkedList(head);
    }
}
```

**Explanation:**
The `reverseLinkedList` function uses three pointers (`prev`, `current`, and `next`) to reverse the direction of pointers in the linked list. The `printLinkedList` function is used to print the original and reversed linked lists for verification.

This question assesses the candidate's understanding of linked lists and their ability to manipulate pointers. It also checks if they are comfortable with basic iterative algorithms.
