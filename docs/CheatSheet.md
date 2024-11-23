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

### Insert Mode:

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


