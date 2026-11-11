# TASK 3: CASE STUDIES WITH PDA AND CFG
## Pushdown Automata and Context-Free Grammar

### Student Details
- **Name:** Dande Durga Prasad
- **Register Number:** RA2411026050066
- **Course:** 21CSC301T – Formal Language and Automata
- **Institution:** SRM Institute of Science and Technology, Tiruchirappalli

---

## Project Overview

This project demonstrates the applications of Pushdown Automata (PDA) and Context-Free Grammar (CFG) through three practical case studies.

The three case studies are:
1. Balanced Parentheses
2. Arithmetic Expression Validation
3. Palindrome Checking

Python is used to implement the validation programs, test cases, stack operations, CFG-to-PDA verification, and PDA diagrams.

## Case Study 1: Balanced Parentheses

**Problem:** Check whether parentheses `()`, square brackets `[]`, and curly brackets `{}` are balanced and properly nested.

**CFG:**
```text
S → BS | B
B → (S) | () | [S] | [] | {S} | {}
```

**PDA Working:**
- Push opening brackets onto the stack.
- Check each closing bracket against the stack top.
- Pop the matching opening bracket.
- Accept if the input ends with an empty stack.

**Examples:**
- `{[()]}` – Accepted
- `([)]` – Rejected

## Case Study 2: Arithmetic Expression Validation

**Problem:** Validate arithmetic expressions using CFG and PDA.

**Ambiguous Grammar:**
```text
E → E + E | E * E | (E) | id
```

**Revised Grammar:**
```text
E  → T E2
E2 → + T E2 | ε
T  → F T2
T2 → * F T2 | ε
F  → (E) | id
```

Multiplication has higher precedence than addition. Parentheses can change the evaluation order.

**Example:**
```text
id + id * id
2 + (3 * 4) = 14
```

## Case Study 3: Palindrome Checking

**Problem:** Check whether a string reads the same from left to right and right to left.

**Unmarked Palindrome CFG:**
```text
S → aSa | bSb | a | b | ε
```

**Marked-Centre CFG:**
```text
S → aSa | bSb | c
```

The unmarked palindrome NPDA guesses the middle using nondeterministic transitions. The marked-centre PDA uses `c` to identify the middle.

**Examples:**
- `ababa` – Accepted by the unmarked palindrome grammar.
- `abcba` – Accepted by the marked-centre grammar.

## Technologies Used
- Python
- Google Colab
- Context-Free Grammar (CFG)
- Pushdown Automata (PDA)
- Matplotlib

## Project Files

| File Name | Description |
|---|---|
| `FLA_TASK_3.ipynb` | Complete Python implementation |
| `balanced_brackets_pda.png` | Balanced brackets PDA diagram |
| `arithmetic_expression_pda.png` | Arithmetic expression PDA diagram |
| `marked_palindrome_dpda.png` | Marked-centre palindrome DPDA diagram |
| `unmarked_palindrome_npda.png` | Unmarked palindrome NPDA diagram |
| `README.md` | Project documentation |

## How to Run the Project

1. Open the notebook using Google Colab.
2. Run all Python code cells.
3. View the test results and PDA diagrams.
4. Check accepted and rejected input strings.

## Conclusion

This project demonstrates how Context-Free Grammars describe context-free languages and how Pushdown Automata use a stack to recognize them.

The three case studies show the applications of PDA and CFG in bracket validation, arithmetic expression parsing, and palindrome checking.

Thus, PDA and CFG are important concepts in compiler design, syntax checking, and formal language processing.

---
**End of Task 3 Project**
