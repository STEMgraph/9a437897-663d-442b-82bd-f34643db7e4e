<!---
{
  "id": "9a437897-663d-442b-82bd-f34643db7e4e",
  "depends_on": ["binary_switch_mapping"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-03-27",
  "keywords": ["boolean algebra", "logic gates", "functions", "truth tables", "binary"]
}
--->

# Introducing Boolean Algebra with Switches and Logic

## 1) Introduction
In the last sheet, we explored how binary inputs (like switches) can be connected to outputs (like LEDs or relays) via **functions**. Now we take a deeper look into the **algebra of logic** — a special kind of math used to describe how combinations of binary states lead to decisions.

This math is called **Boolean Algebra**, named after the mathematician **George Boole**. It uses variables that can only be `0` (false/off) or `1` (true/on), and defines **logical operations** between them.

---

### 1.0.1) Logical Operations
Here are the three most important operations in Boolean algebra:

- **AND** (written as `A AND B`, sometimes `A ∧ B`):
  - Only true if *both* inputs are `1`
  - Truth table:
    ```
    A  B  A AND B
    0  0     0
    0  1     0
    1  0     0
    1  1     1
    ```

- **OR** (written as `A OR B`, sometimes `A ∨ B`):
  - True if *at least one* input is `1`
  - Truth table:
    ```
    A  B  A OR B
    0  0    0
    0  1    1
    1  0    1
    1  1    1
    ```

- **NOT** (written as `NOT A`, or `¬A`, or `~A`):
  - Flips the input: `1` becomes `0`, `0` becomes `1`
  - Table:
    ```
    A  NOT A
    0    1
    1    0
    ```

These rules are the **algebra of logic**. They describe how inputs (switches, sensors) combine and affect outputs.

---

### 1.0.2) Visualizing Boolean Functions with Switches
Let’s imagine again that switches can either be `0` (open) or `1` (closed). We’ll treat each combination as a **variable** and apply logical operations.

Example:
- Let switch A and switch B be inputs.
- Let the light turn on only when *at least one* of them is pressed.
- This is a logical OR: `A OR B`

Another example:
- Let the light turn on only if A is ON and B is OFF.
- This is: `A AND (NOT B)`

---

### 1.0.3) Boolean Expressions as Functions
Boolean expressions are just **functions** with binary inputs and binary outputs.

```
f(A, B) = A AND (NOT B)
```

We can again list all inputs and outputs in a **truth table**:
```
A  B  NOT B  A AND (NOT B)
0  0    1         0
0  1    0         0
1  0    1         1
1  1    0         0
```

---

## 2) Tasks

1. **Explore Boolean OR**: Make a truth table for the expression:
   ```
   f(A, B, C) = A OR B OR C
   ```

2. **Build a Conditional Light**  
   Write a function `f(A, B) = A AND (NOT B)`. Draw the truth table and explain in which situation the output is ON.

3. **Design Your Own Rule**  
   Invent your own rule using A, B, and logical operations (AND, OR, NOT). Write the Boolean expression and draw the truth table for all 4 input combinations.

4. **Combine Three Inputs**  
   Let A, B, C be three switches. Define a Boolean function that turns on a lamp only if exactly **two of them** are ON.

---

## 3) Questions
1. How does Boolean algebra simplify how we describe switch logic?
2. Can every possible binary function be described using AND, OR, and NOT?
3. Why are truth tables useful?
4. What happens to the number of rows in a truth table as you add more inputs?

---

## 4) Final Advice
Boolean algebra gives you a **language** to describe systems that make decisions based on binary inputs. It’s the foundation of all digital logic — from basic electronics to entire CPUs.

> By thinking in terms of truth tables and logic expressions, you can build, analyze, and debug real-world digital systems — even before touching a wire.

The best way to learn Boolean logic is to play with it: try combinations, build truth tables, and imagine the outputs lighting up.

If you're ready, the next step might involve **logic gates** — physical implementations of these Boolean operations.
