---
tags:
  - vim
  - learning
  - teaching
---
## Goals

By the end of this week, you should:
- Understand and use the basic operators (`c`, `C`, `cc`, `d`, `D`, `dd`) to modify and manipulate text.
- Learn how to combine these operators with motions for powerful precise editing.
- Master the `.` (dot) command to repeat the last action, improving efficiency.

---

## Lesson

Operators are commands that act on text. They are not enough on their own and they are usually combined with a motion or text object to define the scope of the operation. For example, `d` (delete) combined with `e` (word motion) deletes till end (`de`). This combination of operators and motions is fundamental to Vim's power and flexibility.

### Operator Pending Mode

Operator-pending mode starts after an operator command, and puts Vim in waiting for a {motion/text-object} to specify the text that the operator will work on. This will become crystal clear with the examples in the next section.

When in operator-pending mode you usually see the operator in the status bar. Press `c` once and check where this is visible in the status bar, the operator won't do anything to the text on its own. You can press Escape to go back to normal mode.

Note: in vscode this is usually where you `-- INSERT --`, but it quickly disappears after the keypress to not clutter the status bar.

### Operators
- `c` ==change== : Deletes the specified text and enters Insert Mode. By default deleted text is also copied into the clipboard (for vim this is a special register - we will cover this later).
	Example: `ce` changes till the end of the word under the cursor.
	TODO Gif example
	
- `d` ==delete== : Deletes the specified text. By default deleted text is also copied.
	Example: `db` deletes back to the beginning of the current word.
	TODO Gif example

Note: hjkl and arrow keys are also navigation commands so you can combine them with the operators.

All this may not seem far too useful yet, but it is laying the foundation for the future and thrust me on this we will soon learn a bit more navigation commands and text objects.

### Shortcuts

Vim provides some very quick shortcuts in combination with the above operators.

- `C` ==Change to end of line== : Deletes everything from the cursor to the end of the line and enters insert mode.
	TODO Gif example
	
- `cc` ==change whole line== : Deletes the entire line and enters insert mode.
	TODO Gif example
	
- `D` ==Delete to end of line== : Deletes from the cursor to the end of the line.
	TODO Gif example
	
- `dd` ==Delete whole line== : Deletes the entire line.
	TODO Gif example
	

You should be seeing the pattern here.

### . (dot command)

The `.` command repeats the last text changing command you executed. This is a key feature of Vim that enhances productivity by reducing repetition and this is one of the major features that really got me into vim in the first place.

Examples:
- After typing `de` to delete till the end of a word, press `.` to delete again.
	TODO Gif example
	
- Navigate to beginning of a word Use `cw` to change word, type something and press Escape, then navigate with `w` to the beginning of the next word and press `.` to repeat the previous change for the word under the cursor.
	TODO Gif example

---

## CheatSheet

**Operators**:
- `c`: change
- `C`: Change to end of line
- `cc`: change line
- `d`: delete
- `D`: Delete to end of line
- `dd`: delete line

**Dot Command**:
- `.`: Repeats the last change command.

---

## Exercise

Here’s a sample text you can use for the exercises:
```
The quick brown fox jumps over the lazy dog. 
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Vivamus luctus urna sed urna ultricies ac tempor dui sagittis. 
Integer vel nisi-id arcu_viverra vehicula eget ac odio.
```

Reminder: When you are in normal mode you can press `u` to undo your last change, you can also use the hjkl keys, arrow keys or the mouse for this exercise

When doing the exercises to better understand how the operators work try to focus on moving horizontally using word motions.

### Operators

#### Exercise: `c`:
    - Use `ce` to replace "quick" with "speedy" in the sentence: `The quick brown fox`.
    - Try `cc` to replace "Lorem ipsum..." line with "Something el–se".
    - Use `C` to replace everything after "fox" in: `The quick brown fox`.

#### Exercise: `d`:
    - Use `de` to delete "quick" in the sentence: "The quick brown fox".
    - Use `dd` to delete the entire second line.
    - Try `D` to delete the content after "brown".

### Repeat
#### Exercise: `.`**:
    - After using `dw`, `db`, `de` or something else, press `.` to delete delete another.
    - navigate to the beginning a of a word change using the `c` operator and motion like `e`, write something, go back to normal mode, then navigate to another word and press `.`, it will repeat the change and 

---

## Practice

**Operators**
- Instead of going straight to insert mode, focus on changing words combining the operators with word motions

**Switching Modes**:
- Don't forget to keep going back to normal mode for navigation after each insert

**Using Word Motions**:
- Keep your focus on navigating horizontally using all word motions.

---

## Further Reading

- [Vim Operators](https://vimhelp.org/)
- [Dot Command](https://neovim.io/doc/user/repeat.html#single-repeat)