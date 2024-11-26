## Goals

By the end of this week, you should:

- Know how to navigate efficiently within a file using commands like `gg`, `G`, and `:line_number`.
- Understand how to jump to a specific percentage of the file with motions like `5%`.
- Combine file navigation motions with operators.

## Lesson

File navigation motions allow you to jump to specific locations in a file without scrolling. These commands make it easy to work in large files by positioning the cursor precisely.

### Motions

**Start and End of the File**

- `gg`: Jump to the beginning of the file. In any position within the file, pressing `gg` moves the cursor to the first line at the start.
- `G`: Jump to the end of the file. In any position within the file, pressing `G` moves the cursor to the last line.

**Specific Line Numbers**

- `10gg` or `10G`: Jump to line 10. Pressing `10gg` `10G` places the cursor at the beginning of line 10.
- `:10`: Jump to line 10 (Command-line mode). Type `:10` and press Enter to move the cursor to line 10.

**Jump to a Percentage**

- `5%`: Jump to 5% of the way through the file.
	- Example: In a file with 100 lines, pressing `5%` places the cursor on line 5.

---

## CheatSheet

- **File Navigation**:
	
	- `gg`: Jump to the start of the file.
	- `G`: Jump to the end of the file.
	- `[line_number]gg ` `[line_number]G` `:[line_number]`: Jump to the specified line.
	- `[number]%`: Jump to the specified percentage of the file.

---

## Exercises

1. Navigate to the start and end of the file:
    
    - Use `gg` to move to the beginning of the file.
    - Use `G` to move to the end of the file.
	
2. Practice jumping to specific lines:
    
    - Use `10gg`, `10G` or `:10` to navigate to line 10.
    - Test with other line numbers in the file.
    - Check which option you prefer the best.
	
3. Explore percentage navigation:
    
    - Experiment with percentage navigation.

---

## Practice

- **File Start and End**: Focus on using `gg` and `G` to quickly reach the top and bottom of the file. Reflect on how these motions minimize scrolling.
- **Line-Specific Navigation**: Practice jumping to specific lines using `[number]G` and `:line_number`. Pay attention to how these motions save time compared to scrolling manually.
- **Percentage-Based Movement**: Use `[number]%` to estimate positions in the file and navigate efficiently. Practice different percentages to get comfortable with this motion.

---

## Further Reading