# Stack

A stack is a linear data structure with a Last In, First Out (LIFO) arrangement. Imagine a stack of plates; you add (push) and remove (pop) them from the top. The last plate placed is the first one you pick. Similarly, a stack efficiently manages data, facilitating operations like function calls and backtracking in algorithms.

In Python, this get's easier to implement, as opposed to C++, because we can use Lists here, instead of Arrays.

Suppose, we have a normal List

l = [1,2]
print("Original List: ", l)
print(l.append(3))
print("Appended List: ", l)
print("Popping element", l.pop())
print("Result List: ", l)


OutPut: 

Original List:  [1, 2]
None
Appended List:  [1, 2, 3]
Popping element 3
Result List:  [1, 2]

So the append built-in method will always add the element to the end of the list.

What if we wanted to add the element at the start of the list????

print("Original List: ", l)
print(l.insert(0,3))
print("After insertion into List: ", l)
print("Popping element: ", l.pop())
print("Result List: ", l)

OutPut:

Original List:  [1, 2]
None
After insertion into List:  [3, 1, 2]
Popping element:  2
Result List:  [3, 1]

With the help of Lists, we can easily implement the Stack Data Structure in a Global Method, for us to implement it anywhere.

Now, I have solved some basic and challenging problems here, with explanation.

For the Solution and Explanation, you will have to look into the code, for better understanding.

DISCLAIMER: These Problems were taken from the internet, resources from FAST NUCES, and the last problem was the most challenging one, that was taken from technical interview questions (personal experience).

## Problem #1: Parentheses Validation

Write a Python function is_valid_parentheses(s) that takes a string s consisting of parentheses '(', ')', '{', '}', '[', ']', 
and determines if the input string has well-formed parentheses. 

The function should return True if the parentheses are well-formed, and False otherwise.

For example: 

>>> is_valid_parentheses("(){}[]")
True

>>> is_valid_parentheses("({[]})")
True

>>> is_valid_parentheses("([)]")
False

>>> is_valid_parentheses("{[()]}")
True

This problem tests your understanding of how to use a stack to check for well-formed parentheses. 

You'll need to iterate through the characters in the string, use a stack to keep track of the opening parentheses, 
and check if each closing parenthesis matches the corresponding opening parenthesis.

## Problem #2: Evaluate Postfix Expression

Write a Python function evaluate_postfix(expression) that takes a string expression representing a postfix expression (also known as Reverse Polish Notation) and returns the result of the expression.

In postfix notation, operators come after their operands. For example, the infix expression "2 + 3" would be written as "2 3 +" in postfix notation.

The postfix expression can contain the following:

Operands: Integers or floating-point numbers.

Operators: '+', '-', '*', '/'

The function should return the result after evaluating the postfix expression.


Example:

>>> evaluate_postfix("23+")
5

>>> evaluate_postfix("52*8+")
18

>>> evaluate_postfix("92/3-")
-1.5

Note:
You can assume that the input expression is a valid postfix expression, and the operands and operators are separated by spaces.

This problem tests your understanding of stack-based evaluation and how to handle operators in postfix notation.

## Problem #3: Largest Rectangle in Histogram

Given an array heights representing the heights of a list of buildings in a histogram, 
find the area of the largest rectangle that can be formed by the histogram.

For exmaple:

heights = [2, 1, 5, 6, 2, 3]
largest_rectangle_area(heights)

Output: 10

Explanation: The largest rectangle is formed by the buildings with heights 5 and 6.

Solve this problem using a stack-based approach. 
The idea is to iterate through the histogram, keeping track of the indices of the buildings in a stack.

When you encounter a building shorter than the one at the top of the stack, pop elements from the stack 
and calculate the area until you find a shorter building or the stack is empty. Keep track of the maximum area encountered during this process.

This problem involves careful handling of indices and heights in a stack to efficiently calculate the area of the largest rectangle in the histogram.
