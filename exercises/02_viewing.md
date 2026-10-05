# Exercise 2 — Viewing Files

**Goals:** Practice `cat`, `less`, `head`, `tail`, wildcard expansion with `*`, and `wc`.

Run these tasks from the repository root.

## Key concepts

- **Text file:** A file containing human-readable characters arranged as lines.
- **Standard output:** The default destination where a command displays its results, usually the terminal.
- **Pager:** A program, such as `less`, that displays a file one screen at a time.
- **Wildcard:** A character the shell uses to match filenames. The `*` wildcard matches any sequence of characters.
- **Concatenation:** Joining the contents of multiple files into a single output stream.

## Commands used

| Command | Purpose |
| --- | --- |
| `cat` | Display or concatenate file contents |
| `less` | View and search a file one screen at a time |
| `head` | Display the beginning of a file |
| `tail` | Display the end of a file |
| `wc` | Count lines, words, and bytes |

## Tasks

- Show the first three lines of `data/raw/sample1.txt`.
- Show the last two lines of `data/raw/sample2.txt`.
- Page through `data/projects/alpha/logs/access.log` and search for `500` within the pager.
- Concatenate all `.txt` files in `data/raw/` into one output stream.
- Count the lines, words, and bytes in `data/raw/sample1.txt`.

## Hints

- `head -n 3`, `tail -n 2`, `cat data/raw/*.txt`
- In `less`, type `/500` and press Enter to search, `n` to find the next match, and `q` to quit.
- Use `wc` with the `-l`, `-w`, and `-c` options.
