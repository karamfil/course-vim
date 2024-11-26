# ⚠️ work in progress
## Goals

By the end of this week, you will:

- Understand how to navigate efficiently through code structures using matching brackets, function definitions, and comment blocks.
- Learn to combine these motions with operators for precise and efficient editing in code.

---
## Lesson

Code navigation in Vim enables you to jump between matching brackets, function definitions, and structural elements like comments. These commands are essential for working efficiently in large codebases or structured files.

### Key Commands

1. **Bracket Matching**
    
    - `%`: Jump between matching brackets, parentheses, or braces.
        - Example: In `(foo(bar))`, pressing `%` moves between the `(` and `)` or `{` and `}`.
2. **Moving to Function or Method Start**
    
    - `]m`: Move to the start of the next method or function.
        - Example: In a file with multiple functions, pressing `]m` jumps to the beginning of the next function.
    - `[m`: Move to the start of the previous method or function.
        - Example: Pressing `[m` jumps to the beginning of the previous function.
3. **Moving to Function or Method End**
    
    - `]M`: Move to the end of the next method or function.
        - Example: In a file with multiple functions, pressing `]M` jumps to the end of the next function.
    - `[M`: Move to the end of the previous method or function.
        - Example: Pressing `[M` jumps to the end of the previous function.
4. **Code Block Navigation**
    
    - `])`: Jump to the next unmatched `)`.
    - `[(`: Jump to the previous unmatched `(`.
    - `]}`: Jump to the next unmatched `}`.
    - `[{`: Jump to the previous unmatched `{`.
5. **Comment Navigation**
    
    - `[/*`: Move to the start of the previous comment block.
    - `]/*`: Move to the start of the next comment block.
6. **Preprocessor Directive Navigation**
    
    - `[#`: Move to the previous preprocessor directive.
    - `]#`: Move to the next preprocessor directive.

---

## CheatSheet

- **Bracket Matching**:
    - `%`: Jump between matching brackets.
- **Function Navigation**:
    - `]m`: Next method or function start.
    - `[m`: Previous method or function start.
    - `]M`: Next method or function end.
    - `[M`: Previous method or function end.
- **Block Navigation**:
    - `])`: Next unmatched `)`.
    - `[(`: Previous unmatched `(`.
    - `]}`: Next unmatched `}`.
    - `[{`: Previous unmatched `{`.
- **Comment Navigation**:
    - `[/*`: Previous comment block.
    - `]/*`: Next comment block.
- **Preprocessor Directive Navigation**:
    - `[#: Previous preprocessor directive.
    - `]#`: Next preprocessor directive.

---

## Exercises

1. Practice bracket matching:
    
    - Use `%` to jump between matching brackets or braces in nested structures.
2. Explore function navigation:
    
    - Use `]m` and `[m` to navigate to the start of functions.
    - Use `]M` and `[M` to navigate to the end of functions.
3. Test block navigation:
    
    - Use `])` and `[(` to jump to unmatched parentheses.
    - Use `]}` and `[{` to navigate unmatched braces.
4. Navigate comments and preprocessor directives:
    
    - Use `[/*` and `]/*` to jump between comment blocks.
    - Use `[#` and `]#` to navigate preprocessor directives in code.

---

## Practice

- **Bracket Matching**: Focus on using `%` to navigate between matching brackets, parentheses, or braces in nested code. Reflect on how it simplifies navigating complex structures.
- **Function and Block Navigation**: Practice moving through functions and code blocks using `]m`, `[m`, `])`, and `[{`. Pay attention to how these motions help in navigating large codebases.
- **Efficient Comment Navigation**: Use `[/*` and `]/*` to jump between comment blocks. Reflect on how this can save time while reviewing documentation or code comments.
- **Evaluate Workflow**: Combine these motions with operators like `d` or `y` to manipulate or extract code sections efficiently.