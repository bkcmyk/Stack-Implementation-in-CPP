# STACK IMPLEMENTATION USING ARRAY

**Aim:**
To study and implement **Stack** using arrays with the following menu options:

* Push
* Pop
* Display
* Exit

**Tools Used:**

* VS Code or any Online C++ Compiler

---

## Theory

A **Stack** is a linear data structure in which elements can be inserted or deleted only from one end, called the **Top**.
It works on the **LIFO (Last In First Out)** principle:

* The element inserted last is the first to be removed.

### Stack Operations

1. **Push** → Insert an element at the top.
2. **Pop** → Remove an element from the top.
3. **Peek/Top** → View the top element without removing it.
4. **Display** → Print all stack elements from bottom to top.

### Representation of a Stack

```
   TOP → [40]   <-- Last inserted (first out)
          [30]
          [20]
   BASE → [10]   <-- First inserted (last out)
```
<img width="1152" height="582" alt="image" src="https://github.com/user-attachments/assets/4e5fc79f-6c22-4c78-8091-0109a4c62f0a" />


### Key Points

* If `top == size - 1` → **Stack Overflow** (stack is full).
* If `top == -1` → **Stack Underflow** (stack is empty).

---

## General Syntax of a Stack in C++

```cpp
class Stack {
    int arr[SIZE];  // Array for storage
    int top;        // Pointer to top element
public:
    Stack();        // Constructor
    void push(int); // Insert element
    int pop();      // Delete element
    int peek();     // Show top element
    void disp();    // Display all elements
};
```

---

## Algorithms

### 1. Push (Insert)

1. Check if `top == size - 1`.

   * If true → print **Stack Overflow**.
2. Otherwise, increment `top`.
3. Place the new element at `arr[top]`.

---

### 2. Pop (Delete)

1. Check if `top == -1`.

   * If true → print **Stack Underflow**.
2. Otherwise, store `arr[top]`.
3. Decrement `top`.
4. Return the deleted value.

---

### 3. Peek (View Top)

1. Check if `top == -1`.

   * If true → print **Stack Underflow**.
2. Otherwise, return `arr[top]`.

---

### 4. Display

1. Check if stack is empty (`top == -1`).

   * If true → print **Stack Underflow**.
2. Otherwise, print all elements from `arr[0]` to `arr[top]`.

---

## Applications of Stack

1. **Function Calls:** System uses call stack for execution.
2. **Expression Evaluation:** Used in compilers for evaluating postfix/prefix expressions.
3. **Undo/Redo Functionality:** Text editors maintain action history using stacks.
4. **Parentheses Matching:** Validating balanced brackets.
5. **Backtracking:** Used in recursion and maze-solving algorithms.

---

## Advantages

* Simple to implement and efficient for LIFO operations.
* Push/Pop operations are **O(1)** (constant time).
* Useful in managing temporary data like recursion and undo functionality.
