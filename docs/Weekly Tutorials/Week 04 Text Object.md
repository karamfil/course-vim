## Goals

By the end of this week, you should:

- Understand the concept of text objects in Vim.
- Learn how to use default text objects for efficient text selection and manipulation.

---

## Lesson

A **text object** is a powerful Vim concept that allows you to operate on a logical unit of text. Text objects are used with operators like `d` (delete), `y` (yank), and `c` (change) to perform actions on specific regions of text, such as words, paragraphs, or blocks.

Text objects are typically used with two components:

A command (e.g., `d` for delete, `c` for change) and the text object (e.g., `iw` for "inner word" or `ap` for "a/around paragraph").

One advantage over the word motions is that you don need to be at the start or beginning of a word to change it, with text object you can be in an arbitrary character of the word.
#### Note

Text objects can be extended with plugins to add more functionality. We will cover such plugins in future weeks.

### Default Text Objects

The default text objects in Vim start with `i` (inner, inside) or `a` (a, around)

`a` and `i` : **a/around and inner/inside**
    
- **`a`** : Includes surrounding delimiters/whitespace (if applicable).
- **`i`** : Excludes surrounding delimiters/whitespace.
	
`p `: **paragraph** is defined as a block of text separated by one or more blank lines. It includes the text up to (but not including) the next blank line or the start/end of the file.
    
- `ap` : A/Around the paragraph (including trailing blank lines).
- `ip` : Inner paragraph (excluding trailing blank lines).

`w` : **word** consists of a sequence of letters, digits and underscores, or a sequence of other non-blank characters, separated with white space (spaces, tabs, `<EOL>`).

- `aw`: Includes the trailing whitespace.
- `iw`: Inner word, excluding the whitespace.

`W` : **WORD** consists of a sequence of non-blank characters, separated with white space.

- `aw`: Includes the trailing whitespace.
- `iw`: Inner word, excluding the whitespace.

`s` : **sentence** is defined as text ending with a sentence-ending punctuation mark (`.`, `!`, or `?`), followed by one or more spaces or the end of the line.

- `as` : Includes trailing whitespace and punctuation.
- `is` : Inner sentence, excluding trailing whitespace and punctuation.

`[`, `(`, `{`, `<` : **Blocks** These are used to operate on various block structures:

- `i(` or `i)` for "inner parentheses"
- `a(` or `a)` for "around parentheses" (including the parentheses).
- `i[` or `i]` for "inner square brackets".
- `a[` or `a]` for "around square brackets" (including the brackets).
- `i{` or `i}` for "inner curly braces".
- `a{` or `a}` for "around curly braces" (including the braces).
- `i<` or `i>` for "inner angle brackets".
- `a<` or `a>` for "around angle brackets" (including the brackets).

`'`, `"`, `` ` `` : **Quoted Strings**
    
- `i'` : for "inside single-quoted" string.
- `a'` : for "a single-quoted" (including the quotes).
- `i"` : for "inside double-quoted" string.
- `a"` : for "a double-quoted" string (including the quotes).
- `` i` ``  : for "inside back-tick-quoted" string
- `` a` ``  : for "a back-tick-quoted" string (including the quotes).

`b`, `B` : **Blocks by Type** - I personally prefer to specify the text object.

- `b` : Operates on a block delimited by `[` or `(`.
- `B` : Operates on a block delimited by `{` or `[`.

`t`: **XML or HTML Tag**
    
- `at` : Select the entire tag, including the opening and closing tags.
- `it` : Select only the content inside the tags.

### Usage Examples

- `ci"`: Change inside double quotes.
	`"quick brown fox"` → `"new content"`.
- `di[`: Delete inside square brackets.
	`[quick brown fox]` → `[]`.

Here is a list from with more examples to better visualize what is possible, this list is not exhaustive, there are far more combinations, feel free to play around:

- `dl` : delete character under the curson
- `dh` : delete character to the left
- `daw` : delete a word
- `diW` : delete inner WORD
- `daW` : delete a WORD
- `das` : delete a sentence
- `dip` : delete inner paragraph
- `dap` : delete a paragraph
- `dib` : delete inner '(...)' block
- `di)` : delete inner '(...)' block
- `dab` : delete a '(...)' block
- `diB` : delete inner '{...}' block
- `di}` : delete inner '{...}' block
- `daB` : delete a '{...}' block

---

## CheatSheet

**General Syntax**: `[operator][a/i][text object]`
- `a` : a/around
- `i` : inner/inside.

Text Objects:
- `p`, `w`, `s` : paragraph, word, sentence.
- `[`, `(`, `{`, `<` : Blocks.
- `'`, `"`, `` ` `` : Quoted strings.
- `b`, `B` : Blocks by type.
- `t` : <tag\> blocks.

---

## Practice

- Text objects are really efficient, focus on figuring out all the places you can utilize them
- Whenever you use a motion think if this motion is efficient enough or can you use a text object to do your change with less effort

- **Using Text Objects**: Focus on identifying scenarios where text objects make your edits faster and more precise. Practice  editing logical chunks of text like paragraphs, sentences, or blocks instead of relying on manual navigation.
- **Inner vs. Around**: Pay close attention to the difference between `i` (inner) and `a` (around). Experiment with when to include or exclude surrounding delimiters for efficient edits.
- **Combining with Operators**: Practice combining text objects with operators like `d`, `c`, and `y`. Aim to minimize the steps needed to perform edits on structured text.
- **Efficiency**: As you use text objects, evaluate whether the motion or text object you chose was the most efficient for the task. Explore alternative text objects when applicable.

---

## Further Reading

- [Neovim Text Objects Documentation](https://neovim.io/doc/user/motion.html#text-objects)
