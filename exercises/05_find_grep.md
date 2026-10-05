# Exercise 5 — Finding files and searching inside files

**Goals:** Use `find` to locate files and `grep` with common options to search file contents.

**Run these tasks from the repository root.**

## Key concepts

- **Search criteria:** Conditions such as name, type, or modification time used to select files.
- **Regular file:** A file containing data, rather than a directory or special filesystem object.
- **Pattern:** Text or a rule used to identify matching filenames or lines.
- **Case-insensitive search:** A search that treats uppercase and lowercase letters as equivalent.
- **Recursive search:** A search that includes all nested directories.

## Commands used

| Command | Purpose |
| --- | --- |
| `find` | Locate files and directories using search criteria |
| `grep` | Search file contents for matching lines |

## Tasks

- Find all regular files ending in `.log` under `data/`.
- Find all regular files modified within the last seven days under `data/`.
- Search all `.log` files under `data/` for lines containing `ERROR`, ignoring case.
- Search `data/projects/alpha/logs/access.log` for requests with HTTP status code `500` and include line numbers.
- Search `data/projects/alpha/logs/access.log` for lines containing `user=` and include line numbers.
- Find empty regular files under `data/tmp/` and review the matches. Do not delete them.

## Hints

- `find data -type f -name '*.log'`
- `find data -type f -mtime -7`
- `grep -ri --include='*.log' 'ERROR' data/`
- `grep -n ' 500 ' data/projects/alpha/logs/access.log`
- `grep -n 'user=' data/projects/alpha/logs/access.log`
- Find empty files with `find data/tmp -type f -empty`.
