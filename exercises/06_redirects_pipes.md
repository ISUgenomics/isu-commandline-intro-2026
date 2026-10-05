# Exercise 6 — Redirects, pipes, and command chaining

**Goals:** Combine commands using output redirection (`>`), pipes (`|`), and command chaining (`;`, `&&`, and `||`).

**Run these tasks from the repository root after completing Exercise 3.**

## Key concepts

- **Redirection:** Sending a command's output to a file instead of the terminal.
- **Pipe:** Sending one command's output directly to another command as input.
- **Command chain:** Multiple commands connected so they run in sequence or according to success or failure.
- **Exit status:** A value indicating whether a command succeeded or failed.

## Operators used

| Operator | Purpose |
| --- | --- |
| `>` | Write standard output to a file, replacing its contents |
| `|` | Pass one command's output to another command |
| `;` | Run the next command regardless of success or failure |
| `&&` | Run the next command only if the previous command succeeds |
| `||` | Run the next command only if the previous command fails |

## Tasks

- Combine all `.txt` files in `data/raw/`, convert the output to uppercase, and save it to `results/all_upper.txt`.
- Extract lines containing the `GET` request method from `data/projects/alpha/logs/access.log`, count them, and write the result to `results/get_count.txt`.
- Skip the header in `data/reports/summary.csv`, extract the `name` values, sort the unique values, and write them to `results/names.txt`.
- Use `;` to print the current directory and then list its contents.
- Chain commands to create `work/step2` and print `OK` only if the directory creation succeeds.
- Try to display a nonexistent file named `missing`; if the command fails, print `failed`.

## Hints

- `cat data/raw/*.txt | tr '[:lower:]' '[:upper:]' > results/all_upper.txt`
- `grep ' GET ' file | wc -l > output-file`
- `tail -n +2 file | cut -d, -f1 | sort -u > output-file`
- `pwd; ls`
- `mkdir -p directory && echo OK`
- `cat missing || echo failed`
