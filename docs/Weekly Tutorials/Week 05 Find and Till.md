## Goals

By the end of this week, you will:

- Understand how to use the `f`, `F`, `t`, and `T` commands to navigate efficiently within a line.
- Learn to use `;` and `,` to repeat find and till motions.
- Combine these commands with `d`, `c`, and the `.` operator to perform powerful and repeatable edits.

## Lesson

The **Find and Till** commands are line-scoped motions that allow you to jump to specific characters or just before them. These commands are useful for precise navigation and editing within a line.

### Find Motions (`f` and `F`)

- **`f<char>`**: find the next occurrence of `<char>` on the current line and places the caret on the `<char>`.
	`The quick brown fox jumps over the lazy dog.`
	
	-  Press `fq`: The cursor moves to the `q` in "quick".

- **`F<char>`**: same as `f` but finding previous `<char>` .
	`The quick brown fox jumps over the lazy dog.`
	
	- Place the cursor at the end of the line and press `Fo`: The cursor moves to the `l` in "lazy".

### Till/To Motions (`t` and `T`)

- **`t<char>`**: find till next occurrence of `<char>` on the current line and places the just before the `<char>`.
	`The quick brown fox jumps over the lazy dog.`

	- Press `tq`: The cursor moves to just before the `q` in "quick".

- **`T<char>`**: same as `t` but for previous `<char>` .
	`The quick brown fox jumps over the lazy dog.`
 
	- Place the cursor at the end of the line and press `Tl`: The cursor moves to just before the `l` in "lazy".

### Repeat Last Find Motions (`;` and `,`)

- **`;`**: Repeat the last `f`, `F`, `t`, or `T` motion in the same direction.
    After pressing `fa` to find the first `a`, press `;` to find the next `a`.

- **`,`**: Repeat the last `f`, `F`, `t`, or `T` motion in the opposite direction.
	After pressing `fa` to find the first `a`, press `,` to go back to the previous `a`.

### Combining with Operators

The **Find (`f`, `F`)** and **Till/To (`t`, `T`)** commands are incredibly versatile when combined with operators like `d` (delete) and `c` (change). These combinations allow you to perform precise edits up to or just before a specific character.

#### Using `d` (Delete)

The `d` operator, combined with Find or Till commands, deletes text from the current cursor position up to the target character.

- `df<char>`: Delete from the cursor up to and including `<char>`.
	In the sentence `The quick brown fox jumps.`, pressing `dfx` deletes `The quick brown fo`, leaving `x jumps.`.
- `dt<char>`: Delete from the cursor up to but **not including** `<char>`.
	In `The quick brown fox jumps.`, pressing `dtx` deletes `The quick brown fo`, leaving `x fox jumps.`.

#### Using `c` (Change)

The `c` operator, combined with Find or Till commands, deletes the text up to the target character and then enters Insert Mode to allow replacing the deleted content.

- `cf<char>`: Change from the cursor up to and including `<char>`.
	In `The quick brown fox jumps.`, pressing `cfx` deletes `The quick brown fox` and enters Insert Mode, allowing you to replace the text.
- `ct<char>`: Change from the cursor up to but **not including** `<char>`.
	In `The quick brown fox jumps.`, pressing `ctx` deletes `The quick brown fo` (excluding `x`) and enters Insert Mode.

### Combining with `.` Operator

The `.` operator repeats the last change. This makes it incredibly powerful when combined with "find" and "till" motions.

#### Example:

1. Press `df,` to delete up to and including the first comma.
2. Press `.` to delete up to and including the next comma.

---

## CheatSheet

**Find and Till/To Commands**:
    
- `f<char>`: Find next `<char>`.
- `F<char>`: Find previous `<char>`.
- `t<char>`: To/Till next `<char>`.
- `T<char>`: To/Till previous `<char>`.
- `;`: Repeat the last `f`, `F`, `t`, or `T` motion in the same direction.
- `,`: Repeat the last `f`, `F`, `t`, or `T` motion in the opposite direction.


---

## Practice

- **Find and Till Commands**: Focus on using `f`, `F`, `t`, and `T` efficiently. Instead of moving manually to a character, train yourself to quickly jump to or just before the target character using these motions.
- **Repeating Motions**: Practice `;` and `,` to repeat Find and Till motions in both directions. Pay attention to how they streamline navigation without retyping commands.
- **Combining with Operators**: Experiment with combining Find and Till commands with `d` and `c`. Think about how you can make edits in a single step without needing to adjust the cursor afterward.
- **Using the `.` Command**: Focus on editing patterns where you can apply the `.` command to repeat changes efficiently. Plan your edits so they can be repeated with minimal input.


---

## Further Reading

- [Vim Motions](https://neovim.io/doc/user/motion.html#object-motions)