## Goals

By the end of this week, you will:

- Learn how to navigate within the visible screen using `H`, `M`, and `L`.
- Understand how to center or reposition the cursor on the screen with `zz`, `zt`, and `zb`.
- Combine these commands with other motions and operators for efficient screen-level navigation and editing.

## Lesson

Screen navigation commands in Vim allow you to move quickly to specific positions within the visible window. These commands are particularly useful for focusing on specific lines or repositioning the cursor without scrolling manually.

### Specific Screen Positions

- `H`: High : places the cursor at the first visible line of the screen. You can use count before the motion `10H` to place the cursor 10 lines from High
- `M`: Middle : places the cursor at the middle visible line of the screen.
- `L`: Low : places the cursor at the last visible line of the screen. You can use count before the motion `10L` to place the cursor 10 lines from Low

### Reposition the Current Line

- `zz`: Zenter : scrolls the file so that the line with the cursor is positioned in the center of the screen.
- `zt`: ZTop : scrolls the file so that the line with the cursor is at the top of the screen.
- `zb`: ZBottom : scrolls the file so that the line with the cursor is at the bottom of the screen.

---

## CheatSheet

**Screen Position**:

- `[count]H`: Jump to the top of the screen.
- `M`: Jump to the middle of the screen.
- `[count]L`: Jump to the bottom of the screen.

**Reposition Cursor**:

- `zz`: Center the current line.
- `zt`: Move the current line to the top.
- `zb`: Move the current line to the bottom.

---

## Exercises

1. Navigate to visible positions:
	
    - Use `H`, `M`, and `L` to quickly move the cursor to the top, middle, and bottom of the visible screen.
    - Combine `H` and `L` with `[count]` to jump to specific line

1. Reposition the current line:
    
    - Use `zz` to center the line with the cursor.
    - Use `zt` and `zb` to move the current line to the top and bottom of the screen.

1. Test combinations:
    
    - Use `H` to jump to the top of the screen, then reposition the cursor line with `zz`.

---

## Practice

- **Screen Positioning**: Focus on using `H`, `M`, and `L` to jump between specific screen positions. Reflect on how they reduce manual scrolling and improve navigation efficiency.
- **Repositioning Lines**: Practice using `zz`, `zt`, and `zb` to reposition the line with the cursor. Pay attention to how each command adjusts the visible screen and makes focused editing easier.
- **Workflow Efficiency**: Experiment with combining screen navigation commands with motions and operators. Evaluate how these commands can streamline your workflow in large or complex files.

---

## Further Reading