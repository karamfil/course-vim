---
tags:
  - vim
  - learning
---
## Modes

- `Esc`: Enter Normal Mode.

## Undo/Redo

- `u`: undo
- `C-r`: redo

## Insert Mode:

- `i`, `I`: insert
- `a`, `A`: append
- `o`, `O`: open line

## Word Motions:

- `w`, `W`: word (with/without punctuation).
- `b`, `B`: back word (with/without punctuation).
- `e`, `E`: end of word (with/without punctuation).
- `ge`, `gE`: end of previous word (with/without punctuation).

## Operators:

- `c`: change
- `C`: Change to end of line
- `cc`: change line
- `d`: delete
- `D`: Delete to end of line
- `dd`: delete line

## Text Objects

**General Syntax**: `[operator][a/i][text object]`
- `a` : a/around
- `i` : inner/inside.

Text Objects:
- `p`, `w`, `s` : paragraph, word, sentence.
- `[`, `(`, `{`, `<` : Blocks.
- `'`, `"`, `` ` `` : Quoted strings.
- `b`, `B` : Blocks by type.
- `t` : <tag\> blocks.

## Find and Till/To Commands:
    
- `f<char>`: Find next `<char>`.
- `F<char>`: Find previous `<char>`.
- `t<char>`: To/Till next `<char>`.
- `T<char>`: To/Till previous `<char>`.
- `;`: Repeat the last `f`, `F`, `t`, or `T` motion in the same direction.
- `,`: Repeat the last `f`, `F`, `t`, or `T` motion in the opposite direction.

## Repeats:
- `.`: Repeat the last change command
- `[number][command]` : repeat command number of times


## Mapping Commands

| Mode    | Normal | Insert | Command | Visual | Selection | Operator | Terminal | Language |
| ------- | ------ | ------ | ------- | ------ | --------- | -------- | -------- | -------- |
| ` `map  | yes    | -      | -       | yes    | yes       | yes      | -        | -        |
| `n`map  | yes    | -      | -       | -      | -         | -        | -        | -        |
| ` `map! | -      | yes    | yes     | -      | -         | -        | -        | -        |
| `i`map  | -      | yes    | -       | -      | -         | -        | -        | -        |
| `c`map  | -      | -      | yes     | -      | -         | -        | -        | -        |
| `v`map  | -      | -      | -       | yes    | yes       | -        | -        | -        |
| `x`map  | -      | -      | -       | yes    | -         | -        | -        | -        |
| `s`map  | -      | -      | -       | -      | yes       | -        | -        | -        |
| `o`map  | -      | -      | -       | -      | -         | yes      | -        | -        |
| `t`map  | -      | -      | -       | -      | -         | -        | yes      | -        |
| `l`map  | -      | yes    | yes     | -      | -         | -        | -        | yes      |


