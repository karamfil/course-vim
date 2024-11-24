


## Goals

By the end of this week, you should:

- Know how to use clipboard-related commands in Vim, such as `c`, `d`, `x`, `y`, and `p`, for cutting, copying, and pasting text.
- Understand the difference between `x` and `X`, as well as `p` and `P`..


---

## Lesson

Clipboard functionality in Vim revolves around cutting, copying, and pasting text, achieved using a combination of operators, motions, and dedicated clipboard commands.

### Cutting/Copying Commands

**Cutting/Changing (`c` and `d`)**

- `c`: Deletes text and enters Insert Mode, we covered this in previous lesson.
- `d`: Deletes text without entering Insert Mode, we covered this in previous lesson.

**Deleting Characters (`x` and `X`)**

- `x`: Deletes the character under the cursor.
- `X`: Deletes the character before the cursor.
	
**Yanking (Copying) (`y`, `Y`, `yy`)**

- `y`: Copies text defined by a motion or text object such as `w`, `iw`, `a{`, etc
- `yy`: Copies the entire line.
- `Y`: Same as `yy` in default configurations. I prefer using `yy` as it follows the logic of `cc` and `dd`

- All of the above command store the copied or deleted text in a register, making it available for pasting.

### Pasting Commands

**Pasting (`p` and `P`)**

- `p`: Pastes text after the cursor (or below the current line in line-wise operations).
- `P`: Pastes text before the cursor (or above the current line in line-wise operations).

### Registers Overview

Every cut, copy, or delete action stores text in a **register**. By default, Vim uses the unnamed register (`"`), which automatically saves the latest text for pasting. We’ll explore registers in greater depth in a future lesson, so don't concern yourself with this for right now

#### Note

By default, change commands (`c`) replace the current clipboard content. This can be frustrating when you want to enter Insert Mode with `c` and paste text, only to find that the clipboard was overwritten by the text you just deleted with the change command, instead of retaining the text you intended to paste. There are different solutions to handle this, which we will cover in future lessons:

- **Plugins**: Some plugins can modify the default behavior of `c` commands to preserve the clipboard content.
- **Visual Mode**: Instead of using `c` to replace text, you can select the text in Visual Mode and then paste directly, ensuring the clipboard content remains intact.

---

## CheatSheet

**Change single character**

- `x` : delete a character under the cursor
- `X` : delete a character before the cursor 

**Yanking**:

- `y` + motion: Yank text.
- `yy` or `Y`: Yank the entire line.
	
**Pasting**:

- `p`: Paste after.
- `P`: Paste before.

---

## Exercise

Use `d` combined with motions to delete specific text:

- Delete a word using `dw` and paste it using `p`.

Practice yanking and pasting:

- Yank a single word with `yw` and paste it using `p`.
- Yank the entire line using `yy` and paste it above using `P`.

Experiment with `x` and `X`:

- Use `x` to delete characters under the cursor.
- Use `X` to delete the character before the cursor.
- Whit this knowledge you can use `xp` to swap 2 characters.

Practice pasting with `p` and `P`, and compare their behavior:

- Paste text after the cursor using `p`.
- Paste text before the cursor using `P`.

---

## Practice

- **Change Commands**: Remember by default change commands `d`, `c`, `x`, and `y` add text to the clipboard (unnamed register)
- **Pasting**: Practice pasting text with `p` and `P`. Pay attention to the positioning of the cursor and how the pasted text aligns relative to the cursor.
- **Evaluate Efficiency**: As you practice, reflect on whether your use of clipboard commands and motions minimizes unnecessary steps. Explore how commands like `yy` or `p` save time compared to manually selecting and inserting text.

---

## Further Reading

