# Question: Validate Parentheses in a String

**Problem Description:**
Write a Java function to determine whether the parentheses in a given string are balanced. The string can contain parentheses ('(', ')'), curly braces ('{', '}'), and square brackets ('[', ']').

**Solution:**

```java
import java.util.Stack;

public class BalancedParentheses {
    // Function to check if parentheses are balanced
    static boolean areParenthesesBalanced(String expression) {
        Stack<Character> stack = new Stack<>();

        for (char ch : expression.toCharArray()) {
            if (ch == '(' || ch == '{' || ch == '[') {
                stack.push(ch);
            } else if (ch == ')' || ch == '}' || ch == ']') {
                if (stack.isEmpty() || !isMatchingPair(stack.pop(), ch)) {
                    return false;
                }
            }
        }

        // Stack should be empty if parentheses are balanced
        return stack.isEmpty();
    }

    // Helper function to check if two parentheses form a matching pair
    static boolean isMatchingPair(char opening, char closing) {
        return (opening == '(' && closing == ')') ||
               (opening == '{' && closing == '}') ||
               (opening == '[' && closing == ']');
    }

    public static void main(String[] args) {
        String expression1 = "{[()]}";
        String expression2 = "([)]";

        System.out.println("Expression 1: " + expression1);
        System.out.println("Are parentheses balanced? " + areParenthesesBalanced(expression1));

        System.out.println("\nExpression 2: " + expression2);
        System.out.println("Are parentheses balanced? " + areParenthesesBalanced(expression2));
    }
}
```

**Explanation:**
The `areParenthesesBalanced` function uses a stack to keep track of opening parentheses, curly braces, and square brackets encountered in the string. When a closing parenthesis is encountered, it checks if it matches the last opening parenthesis on the stack using the `isMatchingPair` function. If there is a mismatch or the stack is not empty after processing the entire string, the parentheses are not balanced.

This question assesses the candidate's understanding of stacks and their ability to use them to solve real-world problems, such as validating expressions.
