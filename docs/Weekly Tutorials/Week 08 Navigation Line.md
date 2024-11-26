## Goals

By the end of this week, you will:

- Understand how to navigate within a line efficiently using `0`, `^`, `$`, and `g_`.
- Learn to move between lines using `+` and `-`.
- Combine these commands with motions and operators for quick and precise text manipulation.

---

## Lesson

Vim provides line navigation commands that allow you to move to specific parts of a line or jump to the start or end. These commands are efficient and work seamlessly with operators like `d`, `y`, and `c`.

### Key Commands

**Within a Line**

- `0`: Move to the beginning of the line.
	In the text `The quick brown fox`, pressing `0` moves the cursor to the `T`.
- `^`: Move to the first non-whitespace character of the line.
	For the line `The quick brown fox`, pressing `^` moves the cursor to the `T` after the spaces.
- `$`: Move to the end of the line.
	In the text `The quick brown fox`, pressing `$` moves the cursor to the `x`.
- `g_`: Move to the last non-whitespace character of the line.
	In the line `The quick brown fox` , pressing `g_` moves the cursor to the `x`, ignoring trailing spaces.
- `|` : TODO
	
**Between Lines**

- `+`: Move to the first non-whitespace character of the **next line**.
	If on `The quick brown fox`, pressing `+` moves the cursor to the start of the next line.
- `-`: Move to the first non-whitespace character of the **previous line**.
	If on `jumps over the lazy dog`, pressing `-` moves the cursor to the start of the previous line.

---

## CheatSheet

**Within the Line**:

- `0`: Start of the line.
- `^`: First non-whitespace character of the line.
- `$`: End of the line.
- `g_`: Last non-whitespace character of the line.

**Between Lines**:

- `+`: First non-whitespace character of the next line.
- `-`: First non-whitespace character of the previous line.

---

## Exercises

Practice moving within a line:

- Use `0` to jump to the beginning of lines.
- Use `^` to skip leading whitespace and move to the first word.
- Use `$` to quickly jump to the end of lines.
- Use `g_` to navigate to the last character of lines, ignoring trailing spaces.

Combine navigation between lines:
    
- Use `+` and `-` to move between lines and position the cursor at the first word of each line.

Test combining with motions:
    
- Delete from the beginning of the line to the first word with `d^`.
- Yank from the current position to the end of the line with `y$`.

---

## Practice

- **Line Navigation**: Focus on using `0`, `^`, `$`, and `g_` for precise cursor placement. Pay attention to how they behave in lines with varying amounts of whitespace.
- **Advanced Line Movement**: Practice moving between lines with `+` and `-`. Reflect on how these commands can simplify line-to-line navigation, especially in multi-line blocks.
- **Efficiency Evaluation**: Combine these commands with operators like `d` or `y` and evaluate whether you’re minimizing cursor movements.

---

## Further Reading