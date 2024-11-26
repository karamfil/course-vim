==⚠️ work in progress==
## Goals

By the end of this lesson, you will:

- Set up a basic Neovim configuration using `init.lua`.
- Create modular configuration files for options, keymaps, and plugin management.
- Install and configure [lazy.nvim](https://github.com/folke/lazy.nvim) as your plugin manager.
- Understand how to structure a Neovim setup.

## Lesson

### Create Init File

The `init.lua` file is the entry point for Neovim's Lua-based configuration. We'll start by creating this file in the Neovim configuration directory.

- Navigate to Neovim's configuration directory:
    - On Linux/MacOS: `~/.config/nvim/`
    - On Windows: `C:\Users\<YourUsername>\AppData\Local\nvim\`
- Create the `init.lua` file.
- Add the following config for the leader keys, we will cover this in future lessons:
    ```lua
    vim.g.mapleader = " "         -- Sets the global leader key, used for creating custom mappings. Default: `space`.
	vim.g.maplocalleader = "\\"   -- Sets the local leader key, often used for buffer-specific mappings. Default: `\`.
    ```

### Configure Options

To keep your configuration modular and easier to maintain, we'll set options as a separate file.

- Create the directory `lua/config/` inside your nvim configuration directory.
- Inside this directory, create a file named `option.lua`.
- Add the following content:
	```lua
	vim.opt.number = true           -- Show line numbers in the gutter
	vim.opt.relativenumber = true   -- Show relative line numbers for easier navigation
	vim.opt.cursorline = true       -- Highlight the line where the cursor is located, improving visibility
	```
- In `init.lua`, require this file:
    ```lua
    require("config.option")
    ```
- Restart neovim extention using the command palette.

### Create Keymaps File

This file will store your custom key mappings.

- Create a file named `keymaps.lua` inside the `lua/config/` directory.
- Leave it empty for now; we’ll populate it in future lessons.
- Require this file in `init.lua`:
    ```lua
	require("config.keymaps")
	```

### Install Lazy.nvim

[lazy.nvim](https://github.com/folke/lazy.nvim) is a powerful and lightweight plugin manager for Neovim.

- reate a file named `lazy.lua` inside the `lua/config/` directory.
- Add the following bootstrap code:
    ```lua
	local lazypath = vim.fn.stdpath("data") .. "/lazy/lazy.nvim"
	if not (vim.uv or vim.loop).fs_stat(lazypath) then
	  local lazyrepo = "https://github.com/folke/lazy.nvim.git"
	  local out = vim.fn.system({ "git", "clone", "--filter=blob:none", "--branch=stable", lazyrepo, lazypath })
	  if vim.v.shell_error ~= 0 then
	    vim.api.nvim_echo({
	      { "Failed to clone lazy.nvim:\n", "ErrorMsg" },
	      { out, "WarningMsg" },
	      { "\nPress any key to exit..." },
	    }, true, {})
	    vim.fn.getchar()
	    os.exit(1)
	  end
	end
	vim.opt.rtp:prepend(lazypath)
	
	-- Setup lazy.nvim
	require("lazy").setup({
	  spec = {
	    { import = "plugins" },
	    { import = "plugins_non_vscode", cond = (function() return not vim.g.vscode end) },
	  },
	  install = { colorscheme = { 'tokyonight' } },
	  checker = { enabled = true },
	})
	```
- Require this file in `init.lua`:
    ```lua
	require("config.lazy")
	```

### Final Init File

At the end your init file should look similar to this:
```lua
vim.g.mapleader = " "         -- Sets the global leader key, used for creating custom mappings. Default: `space`.
vim.g.maplocalleader = "\\"   -- Sets the local leader key, often used for buffer-specific mappings. Default: `\`.

require("config.lazy")
require("config.options")
require("config.keymaps")
```

---

## CheatSheet

Plugin **Lazy.nvim**:
- A plugin manager for Neovim

---

## Practice

- **Lazy.nvim**: Test the lazy.nvim bootstrap code and reflect on how it simplifies plugin management compared to manual installation.

---

## Further Reading

- Neovim Lua Configuration: Official guide for Lua-based configurations.
- [lazy.nvim Documentation](https://github.com/folke/lazy.nvim): Learn more about the features and setup of lazy.nvim.