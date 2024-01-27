# Question: Implement a Stack using Linked List

**Problem Description:**
Implement a stack data structure using a linked list. The stack should support the standard stack operations: push, pop, and isEmpty.

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

public class StackUsingLinkedList {
    private Node top; // top of the stack

    // Constructor to initialize an empty stack
    public StackUsingLinkedList() {
        this.top = null;
    }

    // Function to check if the stack is empty
    public boolean isEmpty() {
        return top == null;
    }

    // Function to push an element onto the stack
    public void push(int data) {
        Node newNode = new Node(data);
        newNode.next = top;
        top = newNode;
        System.out.println(data + " pushed to the stack");
    }

    // Function to pop an element from the stack
    public int pop() {
        if (isEmpty()) {
            System.out.println("Stack is empty");
            return -1;
        }
        int popped = top.data;
        top = top.next;
        return popped;
    }

    // Function to peek at the top element of the stack
    public int peek() {
        if (isEmpty()) {
            System.out.println("Stack is empty");
            return -1;
        }
        return top.data;
    }

    public static void main(String[] args) {
        StackUsingLinkedList stack = new StackUsingLinkedList();

        System.out.println("Is the stack empty? " + stack.isEmpty());

        stack.push(10);
        stack.push(20);
        stack.push(30);

        System.out.println("Top element is " + stack.peek());

        System.out.println(stack.pop() + " popped from the stack");

        System.out.println("Is the stack empty? " + stack.isEmpty());
    }
}
```

**Explanation:**
This code demonstrates the implementation of a stack using a linked list. The `Node` class is used to represent each element in the stack, and the `StackUsingLinkedList` class contains methods for `push`, `pop`, `isEmpty`, and `peek` operations. The main method demonstrates the usage of the stack.

This question assesses the candidate's understanding of data structures, particularly linked lists and how they can be used to implement common operations like stack operations.
