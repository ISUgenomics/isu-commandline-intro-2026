# Exercise 1 — Navigation

**Goals:** Practice `pwd`, `ls`, `cd`, absolute and relative paths, and tab completion.

## Key concepts

- **Current working directory:** The directory in which your shell is currently operating.
- **Path:** The location of a file or directory in the filesystem.
- **Absolute path:** A complete path beginning at the filesystem root (`/`), such as `/work/short_term/username/`.
- **Relative path:** A path interpreted from the current working directory, such as `data/raw/`.
- **Parent directory:** The directory one level above the current directory, represented by `..`.
- **Home directory:** Your personal directory, represented by `~`.
- **Tab completion:** Pressing Tab to automatically complete a partially typed command or path.

## Commands used

| Command | Purpose |
| --- | --- |
| `pwd` | Print the current working directory |
| `ls` | List directory contents |
| `cd` | Change the current working directory |
| `find` | Search for files and directories |

## Tasks

- Print your current directory.
- List all files, including hidden files, with details and human-readable sizes.
- From the repository root, change to `data` using a relative path.
- List only directories recursively from your current location.
- Display your current absolute path, use it to change to `projects/alpha/logs`, and then return to the previous directory.
- Use tab completion when entering at least one path.

## Hints

- `pwd`, `ls -lah`, `cd`, `find . -type d`
- Use `cd -` to return to the previous directory.

