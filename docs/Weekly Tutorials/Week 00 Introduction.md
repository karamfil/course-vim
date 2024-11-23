---
tags:
  - vim
  - teaching
  - learning
---

## Why creating this?
Having used Vim-like keybindings for years in tools like Sublime Text and VSCode, I keep falling in love with its power. I’ve created this course to expand, strengthen and deepen my own understanding of Vim. At some point I decided to share this course and designed it to refine those skills and help you on the same journey.

I like vscode it is great and powerful IDE and for now want to stay in, and use the best of both worlds.

Another reason is, I was not able to find a good tutorial, course or book that covers it for people who do not have the time to directly jump and engulf them fully in vim shroud dropping the productivity tenfold. So I want this to be a slow, smooth and steady transition keeping you on the edge of the comfort zone.

This will make your transition to terminal vim easier should you choose to take this path later.

## Program
We will start with some of the basics to get a good foundation, then move on the some of the things i found most useful to everyday work, some plugins to greatly improve the usability and then we will proceed more advanced, less used or obscure topics.

## Requirements
This course assumes you already know and use VSCode. We’ll leverage its Neovim integration initially to transition seamlessly into a more Vim-centric workflow.

## What is (Neo)Vim
im is a **modal text editor**, which means it uses different modes for editing, navigating, and interacting with text. Neovim, a modern fork of Vim, enhances this experience with improved features, extensibility, and support for Lua scripting.

- **[Read more about Neovim](https://neovim.io/doc/user/intro.html)**

### **Modes**

Vim operates in different modes, each designed for specific tasks:

| **Mode**              | **Description**                                                                   |
| --------------------- | --------------------------------------------------------------------------------- |
| **Normal Mode**       | ==Default mode==. Navigate and perform text manipulation commands without typing. |
| **Insert Mode**       | Type and insert text like in regular editors.                                     |
| **Visual Mode**       | Select text for manipulation or editing.                                          |
| **Command-line Mode** | Execute commands like saving, searching, or quitting (`:`).                       |
| **Replace Mode**      | Overwrite text as you type.                                                       |

Switching between these modes might feel strange at first, but it’s key to Vim’s efficiency. The separation of navigation and editing minimizes the need for hand movement.

- **[Read more about Vim modes](https://vimdoc.sourceforge.net/htmldoc/intro.html#vim-modes)**

## Why learn Vim?
- **Increased Speed and Efficiency**: Once you master Vim, you can perform complex edits and navigate codebases faster than in traditional editors or IDEs.
- **Keyboard-Centric Workflow**: Vim minimizes reliance on the mouse, keeping your hands on the keyboard and improving focus.
- **Universal Availability**: Vim is installed by default on most UNIX systems and can be used in remote development environments.
- **Customizability**: Vim’s flexibility allows you to tailor your editor to suit your exact needs.
- **Endless Growth**: Learning Vim is a lifelong skill. As you master the basics, you can continually discover more advanced techniques and workflows.

---

## Vim is not hard - it is intuitive

At first glance, Vim might seem complicated - "so many keys to remember". You may have heard jokes about people getting “stuck” in Vim or struggling to quit the editor. However, these stories come from misunderstanding how Vim works.

Vim’s design is **logical and mnemonic**:
- Most commands reflect their purpose: `d` stands for "delete", `c` for "change", and so on.
- Text objects and motions (like `ciw` to "change inner word") are intuitive once you understand the language.

**Think of Vim as learning a new language:**
- Initially, you might struggle to express yourself.
- With practice, you’ll build fluency and start thinking in Vim commands naturally.

Patience and consistent practice will help you overcome the learning curve.

## How we are going to learn?

I am a strong believer that the best way to learn anything is by **consistent practicing**. 

Here we will:
- Introduce small, manageable topics per weekly basis.
- Build upon what’s comfortable (vscode) and expand into new concepts, the idea is to not overwhelm our brain with a ton of new things we will forget tomorrow, but rather retain the knowledge
- Stay productive while learning, ensuring you understand the **what**, **why**, and **how** of everything we will do.

Each week will include:
- **Goals**: Clear objectives for what you’ll learn.
- **Lesson**: Material we will learn for the week.
- **CheatSheet**: We will be building our own cheatsheet
- **Practice**: Practical tasks to apply new skills and solutions with explanations.
- **Further Reading**: Resources to expand and deepen your understanding.

We’ll start with a **clean factory Neovim configuration** in VSCode. Later, we’ll gradually introduce customizations and plugins to help you create a personalized, efficient editing environment.

### Pro Tip: Stay Consistent
- Use sticky notes or a whiteboard to remind yourself of weekly goals, cheatsheet and what you are currently learning. I keep about 5 stickies on my monitor each for 1 week.
- Focus on practicing the current material until it feels natural - this way you will build muscle memory and become efficient

## Setup

To get started, follow these step:

1. **Set up Neovim**:
    - Visit [Neovim Installation Guide](https://neovim.io/) to install Neovim for your operating system.
    - Open a terminal and type `nvim`. If it launches, your setup is correct.
    - type `:q!` to exit 🤣
    
1. **Set up VSCode-Neovim**:
    - Open VSCode, go to the Extensions Marketplace, and install the [VSCode-Neovim extension](https://marketplace.visualstudio.com/items?itemName=asvetliakov.vscode-neovim).
    - In VSCode settings (`Ctrl+,` or `Cmd+,`), search for "Neovim Path."
    - Enter the path to the Neovim executable (e.g., `/usr/bin/nvim` or `C:\Program Files\Neovim\bin\nvim.exe`).
	    - you can find this by typing `which nvim` in the terminal
	    - Open any file in VSCode and verify that Neovim keybindings work as expected.
		    - ex: press `j` a few times the cursor should move down
		- If you press `i` you will enter ==insert== mode and you can mostly use VSCode as without the neovim extension, navigating with arrow keys, typing, etc.
		- If you press esc you will go back to ==normal== mode
## Further Reading

### Online Resources
- [Vim Help](https://vimhelp.org/) – Official Vim documentation.
- [Neovim Documentation](https://neovim.io/doc/)

### Cheat Sheets
- [Vim Cheat Sheet by Roger Petris](https://vim.rtorr.com/)
- [Vim Cheat Sheet by Devhints](https://devhints.io/vim)–

### Books
- [Practical Vim: Edit Text at the Speed of Thought](https://pragprog.com/titles/dnvim2/practical-vim-second-edition/) by Drew Neil.
- [Modern Vim](https://pragprog.com/titles/modvim/modern-vim/) by Drew Neil.

