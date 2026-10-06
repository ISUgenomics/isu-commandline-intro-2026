# Exercise 3 — Working with directories and files

**Goals:** Practice `mkdir`, `cp`, `mv`, `rm`, `ln`, recursive operations, and creating a basic shell script.

**Run these tasks from the repository root.**

## Key concepts

- **Directory:** A container used to organize files and other directories.
- **Recursive operation:** An operation applied to a directory and everything inside it.
- **Symbolic link:** A special file that points to another file or directory.
- **Shell script:** A text file containing commands that a shell can execute.
- **Shebang:** The first line of a script, beginning with `#!`, that identifies its interpreter.
- **Destination:** The location to which a file or directory is copied or moved.

## Commands used

| Command | Purpose |
| --- | --- |
| `mkdir` | Create directories |
| `cp` | Copy files or directories |
| `mv` | Move or rename files or directories |
| `rm` | Remove files or directories |
| `ln` | Create hard or symbolic links |

## Tasks

- Create `work/step1`, `results`, and `scripts`.
- Copy all `.txt` files from `data/raw/` to `work/step1/`.
- Move `data/tmp/placeholder.txt` into `work/`.
- Recursively copy `data/projects/alpha` into `work/alpha_copy/`.
- Copy `data/raw/sample1.txt` to `work/delete-me.txt`, and then remove the copy.
- Using a text editor, create `scripts/EchoScript.sh` with the following contents:

  ```bash
  #!/usr/bin/env bash
  echo "You've added this script to PATH!"
  ```

- In `scripts/`, create a symbolic link named `echo-script.sh` that points to `EchoScript.sh`.

## Hints

- `mkdir -p`, `cp`, `cp -r`, `mv`, `rm`, `ln -s`
- Use `ln -s EchoScript.sh scripts/echo-script.sh` to create a working relative symbolic link.
- Enclose paths containing spaces in quotes.
