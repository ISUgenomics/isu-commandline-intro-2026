# Exercise 4 — Permissions and ownership

**Goals:** Read file permissions and ownership information with `ls -l`, and modify permissions with `chmod`.

**Run these tasks from the repository root after completing Exercise 3.**

## Key concepts

- **Owner:** The user account that owns a file or directory.
- **Group:** A collection of users that can share file permissions.
- **Permissions:** Rules controlling who can read (`r`), write (`w`), or execute (`x`) a file or directory.
- **Execute permission:** Permission to run a script or program; on a directory, permission to access its contents.

## Commands used

| Command | Purpose |
| --- | --- |
| `ls -l` | Display permissions, ownership, and other file details |
| `chmod` | Change file or directory permissions |

## Tasks

- List the permissions and ownership details for everything in `work/step1/`.
- Remove your write permission from `work/step1/sample1.txt`.
- Add execute permission for yourself to `scripts/EchoScript.sh`.
- Remove execute permission for yourself from `work/alpha_copy/logs/access.log`.
- Restore your write permission on `work/step1/sample1.txt`.

## Hints

- In symbolic mode, `u` means owner, `+` adds a permission, and `-` removes one.
- `ls -l`, `chmod u-w file`, `chmod u+x script.sh`, `chmod u-x file`
- Restore write permission with `chmod u+w file`.
