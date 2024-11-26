# ⚠️ work in progress
## Goals

By the end of this week, you will:

- Install and configure the Mini Surround plugin using Lazy.nvim.
- Learn how to use Mini Surround commands for adding, deleting, finding, highlighting, and replacing surrounding characters or blocks.
- Understand the customization options provided by Mini Surround and their mappings.
- Explore similar plugins for surrounding functionality in Neovim.

## Lesson

Let's start with out first plugin, the **Mini Surround** plugin allows you to manipulate surrounding characters (e.g., parentheses, brackets, quotes, tags) efficiently. It offers highly customizable mappings and functionality for adding, deleting, finding, and replacing surroundings.

### Installation with Lazy.nvim

- Create the file `lua/config/plugins/mini.surround.lua`.
- Add the following content to configure and install Mini Surround:    
    ```lua
    return {
	    "echasnovski/mini.surround",

	    opts = {
	        highlight_duration = 5000, -- keep the highlight for 5 secods before clearing
	        mappings = {
	            add = 'sa', -- Add surrounding
	            delete = 'sd', -- Delete surrounding
	            replace = 'sr', -- Replace surrounding

	            find = 'sf', -- Find surrounding
	            find_left = 'sF', -- Find surrounding (to the left)
	            highlight = 'sh', -- Highlight surrounding
	            update_n_lines = 'sn', -- Update `n_lines`

	            suffix_last = 'l', -- Suffix to search with "prev" method
	            suffix_next = 'n', -- Suffix to search with "next" method
	        },
	        search_method = 'cover_or_nearest',
	    }
	}
	```
- Save the file. Lazy.nvim will automatically detect and load this plugin during its setup.

### Key Commands and Operators

**Adding Surroundings (`sa`)**
    
- `sa` : Surround Add : Add a surrounding to the selected text in Normal or Visual Mode.
	- Example: Select `word` and use `sa` followed by `(` to make `(word)`.

**Deleting Surroundings (`sd`)**
    
- `sd`: Delete the surrounding characters around the cursor.
	- Example: From `(word)`, place the cursor inside and use `sd` to make `word`.

**Replacing Surroundings (`sr`)**
    
- `sr`: Replace the current surrounding with a new one.
	- Example: Replace `"word"` with `[word]` by using `sr` followed by the target surrounding.

**Highlighting Surroundings (`sh`)**
    
- `sh`: Highlight the surrounding characters around the cursor for easy visualization.


```
WORK IN PROGRESS

**Finding Surroundings (`sf` and `sF`)**
    
- `sf`: Find the nearest surrounding to the right of the cursor.
- `sF`: Find the nearest surrounding to the left of the cursor.

**Updating Lines (`sn`)**
    
- `sn`: Update the number of lines used to detect surroundings.

**Suffixes (`l` and `n`)**
    
- `l`: Search using the "last" method for surroundings.
- `n`: Search using the "next" method for surroundings.
```

---

## CheatSheet

- **Commands**:
    - `sa`: surround add
    - `sd`: surround delete
    - `sr`: surround replace

    - `sh`: surround highlight
    - `sf`: surround find right.
    - `sF`: surround find left.
    - `sn`: Update detection range for surroundings.
    - `l`: Search "last" surrounding.
    - `n`: Search "next" surrounding.

---

## Exercises

**Adding Surroundings**:
    
- Add parentheses to the word `example` using `sa`.
- Add quotes to the sentence `this is a test`.
    
**Deleting Surroundings**:
    
- Delete the parentheses in `(text)` using `sd`.
- Remove the quotes from `"hello"` using `sd`.
    
**Replacing Surroundings**:
    
- Replace brackets `[content]` with curly braces `{content}` using `sr`.

**Exploring Highlighting and Finding**:
    
- Use `sh` to highlight surroundings in a block of text.
- Use `sf` and `sF` to find surrounding characters in both directions.

---

## Practice

- **Experiment with Surroundings**: Focus on adding, deleting, and replacing surroundings efficiently. Pay attention to how different mappings streamline your workflow. Combine these with inner and around text objects
- **Visualization**: Use `sh` to highlight and better understand the scope of selected surroundings.
- **Directional Searches**: Practice using `sf`, `sF`, `l`, and `n` to navigate surroundings quickly in both directions.

---

## Further Reading

- [Mini Surround Plugin Documentation](https://github.com/echasnovski/mini.surround): Learn more about the plugin's functionality and customization.

- **Similar Plugins**:
    - [vim-surround](https://github.com/tpope/vim-surround): A classic plugin for managing surroundings in Vim.
    - [nvim-surround](https://github.com/kylechui/nvim-surround): A modern Lua-based alternative to vim-surround with additional features.
	- [machakann/vim-sandwich](https://github.com/machakann/vim-sandwich)