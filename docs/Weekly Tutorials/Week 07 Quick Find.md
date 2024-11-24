## Goals

By the end of this week, you will:

- Learn how to use the `*` and `#` commands for quick keyword searches.
- Understand how `n` and `N` help navigate through search results efficiently.
- Combine these commands to quickly locate and navigate instances of text.

---

## Lesson

Quick Find commands in Vim allow you to search for keywords under the cursor or navigate to previous searches without typing. These commands are fast, efficient, and require minimal input.

### Key Commands

**Search for Current Word (`*` and `#`)**
    
- `*`: Searches forward for the word under the cursor.
	If your cursor is on the word `fox` in `The quick brown fox jumps`, pressing `*` highlights the next occurrence of `fox`.
- `#`: Searches backward for the word under the cursor.
	If your cursor is on the word `fox`, pressing `#` highlights the previous occurrence of `fox`.
 
 **Navigate Search Results (`n` and `N`)**
    
- `n`: Moves to the next search result in the direction of the last search.
	After pressing `*` to search forward, `n` continues moving to subsequent matches.
- `N`: Moves to the previous search result, reversing the direction of the last search.
	If you searched forward with `*`, pressing `N` moves to the previous match instead.

### Combining Quick Find Commands

- Use `*` or `#` to initiate the search and locate the first occurrence of the word.
- Use `n` to continue in the same direction or `N` to reverse direction through matches.
- These commands work seamlessly within the current file, making it easy to navigate repetitive patterns.

---

## CheatSheet

**Search Commands**:

- `*`: Search forward for the word under the cursor.
- `#`: Search backward for the word under the cursor.

**Navigation Commands**:

- `n`: Move to the next match in the direction of the last search.
- `N`: Move to the previous match in the opposite direction.

---

## Exercises

Practice locating words:

- Place the cursor on a word and press `*` to search forward for all occurrences.
- Use `#` to search backward for the same word.

Navigate matches:

- After searching with `*`, use `n` to jump through matches.
- Press `N` to reverse direction and move to previous matches.

Test your workflow:

- In a block of text with repeated words, use `*` or `#` to find a word and combine it with `n` and `N` to explore all instances of the word efficiently.

---

## Practice

- **Initiating Searches**: Focus on using `*` and `#` to quickly search for a word without typing. Get used to how they behave relative to the cursor position.
- **Navigating Search Results**: Practice switching directions with `n` and `N`. Pay attention to how they follow or reverse the direction of the initial search.

---

## Further Reading