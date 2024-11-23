## Goals

By the end of this week, you should:

- Understand how to use numbers to repeat a command multiple times.
- Learn how to numbers with motions and operators to perform efficient text editing.
- Practice using numbers in combination with the `.` command for even greater efficiency.

---

## Lesson

In Vim, you can precede most commands with a number to repeat them that many times. Repeats can be applied to motions, operators, macros, and even combined with the `.` command to repeat sequences of actions efficiently.

### Using Repeat Counts with Basic Commands

**Basic Motion Keys with Repeat Count**: Repeats allow you to move multiple times with a single command.

- `5j`: Move down 5 lines.
- `3w`: Move forward 3 words.
- `7h`: Move left 7 characters.

**Insert Mode with Repeat Count**: While repeat counts are less common for Insert Mode commands, they can be used to create multiple lines.

- `15i` : repeat this insert 15 times. An example would be using dash `15i-Esc` -> this will create `---------------`
- `5o`: Create the same insert with 5 new lines below the current one.

**Operators with Repeat Count**: Combine operators with repeat counts to act on larger portions of text.

- `d2w`: Delete 2 words starting from the cursor.
- `3dd`: Delete 3 lines

### Combining Repeat Counts with the `.` Command

The `.` command repeats the last change command, and it works seamlessly with repeat counts. For example:

- Use `d2w` to delete 2 words.
- Press `.` to delete the next 2 words.
- Combining this with a repeat count, like `3.`, however to repeat the action changing the number for example `3.` will do `d3w`.

---

## Practice

- **Using Repeats/Counts with Motions**: Focus on combining repeat counts with motions like `j`, `w`, and `e`. Practice navigating efficiently by using counts instead of repeating motions multiple times.
- **Repeat Counts with Operators**: Work on combining repeat counts with operators like `d`, `c`, and `y`. Focus on editing multiple words or lines in a single command to streamline your workflow.
- **Integrating the `.` Command**: Pay attention to how repeat counts can enhance the effectiveness of the `.` command. Practice planning edits so you can repeat them logically and efficiently with `.`.
- **Efficiency Evaluation**: As you use repeat counts, evaluate if the number you chose is optimal for the task or if a different motion/operator combination would be more efficient.
