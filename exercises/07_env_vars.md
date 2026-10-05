# Exercise 7 — Environment and variables

**Goals:** Inspect `HOME` and `PATH`, and create and export shell variables.

**Run these tasks from the repository root.**

## Key concepts

- **Shell variable:** A named value available in the current shell.
- **Environment variable:** A variable exported to commands and child processes started by the shell.
- **`HOME`:** The environment variable containing the path to your home directory.
- **`PATH`:** A colon-separated list of directories the shell searches for commands.
- **Subshell:** A new shell process started from the current shell.

## Commands used

| Command | Purpose |
| --- | --- |
| `echo` | Display text or variable values |
| `export` | Make a variable available to child processes |
| `find` | Search for files and directories |
| `bash -c` | Run a command in a new Bash subshell |

## Tasks

- Print the values of `HOME` and `PATH`.
- Append the absolute path of `scripts/` to `PATH` for the current shell session.
- Create a variable named `DATA_DIR` containing the absolute path of `data/`, and use it to find all `.csv` files below that directory.
- Export `DATA_DIR`, start a subshell, and print its value from within that subshell.
- Change to a different directory and run `EchoScript.sh` by name to verify the updated `PATH`.

## Hints

- `echo "$HOME"` and `echo "$PATH"`
- `export PATH="$PATH:$(pwd)/scripts"`
- `DATA_DIR="$(pwd)/data"`
- `find "$DATA_DIR" -type f -name '*.csv'`
- `export DATA_DIR`
- `bash -c 'echo "$DATA_DIR"'`
- `(cd "$HOME" && EchoScript.sh)`
