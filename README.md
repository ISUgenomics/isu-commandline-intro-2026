# Introduction to the Command Line

**Instructor:** Viswanathan Satheesh

**Affiliation:** Bioinformatics Facility, Iowa State University

**Contact:** bioinformatics@iastate.edu | satheesh@iastate.edu

- Focus: CLI concepts, navigation, file viewing and operations, permissions, search, redirection, pipes, and environment variables

## Quick start to access the workshop environment

- Open [VS Code Server on Nova OnDemand](https://nova-ondemand.its.iastate.edu/) in a browser.

  ```
  Account: short_term
  Partition: interactive
  ```

- Create your working directory if it does not already exist:

  ```bash
  cd /work/short_term/
  mkdir -p "$USER"
  ```

- In VS Code, select **File → Open Folder**, then open `/work/short_term/<your username>/`.

- Clone the Git repository and enter its root directory:

  ```bash
  git clone https://github.com/ISUgenomics/isu-commandline-intro-2026.git
  cd isu-commandline-intro-2026
  ```

- Confirm that the included workshop data is available:

  ```bash
  ls data
  ```

## Layout

- `exercises/` — step-by-step workshop tasks
- `scripts/` — sample shell script
- `solutions/` — reference answers
- `data/` — instructor-provided sample inputs required by the exercises

## Exercises

1. [Navigation](exercises/01_navigation.md)
2. [Viewing Files](exercises/02_viewing.md)
3. [Working with Directories and Files](exercises/03_files_dirs.md)
4. [Permissions and Ownership](exercises/04_permissions.md)
5. [Finding Files and Searching Inside Files](exercises/05_find_grep.md)
6. [Redirects, Pipes, and Command Chaining](exercises/06_redirects_pipes.md)
7. [Environment and Variables](exercises/07_env_vars.md)
