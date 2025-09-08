# Dart Control Flow Statements

Control flow statements in Dart, such as loops and conditionals, are essential for executing code based on specific conditions or repeatedly until a condition is met. Below is an overview of the `for`, `while`, `do-while`, `switch`, `break`, and `continue` statements with examples and explanations.

### For Loop
The `for` loop is used to execute a block of code a specific number of times. It's useful when the number of iterations is known beforehand.


---

### Example Dart Program
```

void main() {
for (int i = 0; i < 5; i++) {
print('Iteration: $i');
}
}

```

---


- Initializes `i` to 0 and continues as long as `i < 5`.
- After each iteration, `i` is incremented by 1.
- Prints iteration numbers from 0 to 4.

### While Loop
The `while` loop executes a block of code as long as the specified condition is true.


### Example Dart Program
```

void main() {
int count = 0;
while (count < 5) {
print('Count: $count');
count++;
}
}

```

---

- Checks condition `count < 5`.  
- Runs the block and increments `count` each iteration.  
- Prints numbers from 0 to 4.

### Do-While Loop
The `do-while` loop ensures the block of code is executed at least once before checking the condition.

---

### Example Dart Program
```


void main() {
int count = 0;
do {
print('Count: $count');
count++;
} while (count < 5);
}

```

---


- Executes the block first, then checks `count < 5`.  
- Prints numbers from 0 to 4, guaranteeing at least one execution.

### Switch Statement
The `switch` statement evaluates a value against multiple cases and executes the matching one.

---

### Example Dart Program
```


void main() {
var day = 3;
switch (day) {
case 1:
print('Monday');
break;
case 2:
print('Tuesday');
break;
case 3:
print('Wednesday');
break;
default:
print('Invalid day');
}
}

```

---


- Compares `day` with each case.  
- Matches `3` and prints "Wednesday".  
- `break` exits the statement after executing a case.

### Break Statement
The `break` statement exits a loop or `switch` early.

---

### Example Dart Program
```

void main() {
for (int i = 0; i < 10; i++) {
if (i == 5) {
break;
}
print(i);
}
}

```

---


- Prints numbers 0 to 4.  
- Exits the loop when `i == 5`.

### Continue Statement
The `continue` statement skips the current loop iteration and continues with the next.

---

### Example Dart Program
```

void main() {
for (int i = 0; i < 5; i++) {
if (i == 2) {
continue;
}
print(i);
}
}

```

---

- Skips printing when `i == 2`.  
- Prints 0, 1, 3, and 4.

### Summary
- **For Loop:** Executes code a fixed number of times.  
- **While Loop:** Executes while a condition is true.  
- **Do-While Loop:** Executes at least once before checking the condition.  
- **Switch Statement:** Selects execution path based on value matching.  
- **Break:** Exits loop or switch prematurely.  
- **Continue:** Skips current iteration and jumps to the next.


