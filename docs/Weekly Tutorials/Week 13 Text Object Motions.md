==⚠️ work in progress==

## Goals

By the end of this week, you will:

- Understand how to use text object motions to navigate through sentences, paragraphs, and blocks of text.
- Learn how to move efficiently between parentheses and braces using motions like `(`, `)`, `{`, and `}`.
- Navigate structured blocks of text using motions like `]]`, `][`, `[[`, and `[]`.

## Lesson

Text object motions in Vim allow you to navigate structured and logical sections of text, such as sentences, paragraphs, and blocks. These motions are indispensable for working efficiently in code or formatted text files.

### Key Commands

1. **Sentence Navigation**
    
    - `(`: Move to the beginning of the current or previous sentence.
        - Example: In `Hello. |This is a sentence.`, pressing `(` moves the cursor to `Hello.`.
    - `)`: Move to the beginning of the next sentence.
        - Example: In `Hello. |This is a sentence.`, pressing `)` moves the cursor to `This is a sentence.`.
2. **Paragraph Navigation**
    
    - `{`: Move to the beginning of the current or previous paragraph.
        - Example: In the text:
            
            text
            
            Copy code
            
            `Paragraph one.  Paragraph |two.`
            
            Pressing `{` moves the cursor to `Paragraph one.`.
    - `}`: Move to the beginning of the next paragraph.
        - Example: In the same text, pressing `}` moves the cursor to the line after `Paragraph two.`.
3. **Block Navigation**
    
    - `[[`: Move to the beginning of the current or previous block.
        
        - Example: In a code block:
            
            text
            
            Copy code
            
            `if (condition) {     // |Code block }`
            
            Pressing `[[` moves to `if (condition) {`.
    - `]]`: Move to the beginning of the next block.
        
        - Example: In the same code block, pressing `]]` moves to the next block's start.
    - `[]`: Move to the beginning of the previous unmatched `[` or `{`.
        
        - Example: From inside a nested block, `[]` moves to the matching outer block's start.
    - `][`: Move to the beginning of the next unmatched `[` or `{`.
        
        - Example: Inside a deeply nested block, `][` jumps to the next outer block.

---

## CheatSheet

- **Sentence Navigation**:
    - `(`: Move to the start of the current or previous sentence.
    - `)`: Move to the start of the next sentence.
- **Paragraph Navigation**:
    - `{`: Move to the start of the current or previous paragraph.
    - `}`: Move to the start of the next paragraph.
- **Block Navigation**:
    - `[[`: Move to the start of the current or previous block.
    - `]]`: Move to the start of the next block.
    - `[]`: Move to the previous unmatched `[` or `{`.
    - `][`: Move to the next unmatched `[` or `{`.

---

## Exercises

1. Practice sentence navigation:
    
    - Use `(` to move to the start of each sentence in a paragraph.
    - Use `)` to navigate to the next sentence.
2. Explore paragraph motions:
    
    - Use `{` to move back through paragraphs in a multi-paragraph text.
    - Use `}` to move forward through paragraphs.
3. Work with blocks:
    
    - In a code file, use `[[` and `]]` to navigate to different blocks of code.
    - Use `[]` and `][` to jump between nested or unmatched brackets.

---

## Practice

- **Sentence and Paragraph Navigation**: Focus on moving efficiently through structured text using `(`, `)`, `{`, and `}`. Evaluate how these motions simplify jumping between sentences and paragraphs without manual scrolling.
- **Block Navigation**: Practice navigating through structured blocks of text or code using `[[`, `]]`, `[]`, and `][`. Reflect on how these commands reduce the effort of jumping between nested sections.
- **Workflow Efficiency**: Combine text object motions with operators like `d` or `y` to delete or yank entire sentences, paragraphs, or blocks. Experiment with different motions to optimize your workflow.

---

## Further Reading

