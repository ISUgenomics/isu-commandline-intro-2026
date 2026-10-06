# Reference Answers

These are example solutions; many variants are valid.

## 01 Navigation

- `pwd`
- `ls -lah`
- `cd data`
- `find . -type d`
- `pwd`
- `cd "$(pwd)/projects/alpha/logs"`
- `cd -`
- For tab completion, type part of a path, such as `cd pro`, and press Tab.

## 02 Viewing

- `head -n 3 data/raw/sample1.txt`
- `tail -n 2 data/raw/sample2.txt`
- Run `less data/projects/alpha/logs/access.log`, type `/500`, and press Enter. Use `n` for the next match and `q` to quit.
- `cat data/raw/*.txt`
- `wc -l -w -c data/raw/sample1.txt`

## 03 Files and Directories

- `mkdir -p work/step1 results scripts`
- `cp data/raw/*.txt work/step1/`
- `mv data/tmp/placeholder.txt work/`
- `cp -r data/projects/alpha work/alpha_copy`
- `cp data/raw/sample1.txt work/delete-me.txt`, followed by `rm work/delete-me.txt`
- Create `scripts/EchoScript.sh` in a text editor with these contents:

  ```bash
  #!/usr/bin/env bash
  echo "You've added this script to PATH!"
  ```

- `ln -s EchoScript.sh scripts/echo-script.sh`

## 04 Permissions

- `ls -l work/step1/`
- `chmod u-w work/step1/sample1.txt`
- `chmod u+x scripts/EchoScript.sh`
- `chmod u-x work/alpha_copy/logs/access.log`
- `chmod u+w work/step1/sample1.txt`

## 05 Find and Grep

- `find data -type f -name '*.log'`
- `find data -type f -mtime -7`
- `grep -ri --include='*.log' 'ERROR' data/`
- `grep -n ' 500 ' data/projects/alpha/logs/access.log`
- `grep -n 'user=' data/projects/alpha/logs/access.log`
- `find data/tmp -type f -empty`

## 06 Redirects, Pipes, and Chaining

- `cat data/raw/*.txt | tr '[:lower:]' '[:upper:]' > results/all_upper.txt`
- `grep ' GET ' data/projects/alpha/logs/access.log | wc -l > results/get_count.txt`
- `tail -n +2 data/reports/summary.csv | cut -d ',' -f 1 | sort -u > results/names.txt`
- `pwd; ls`
- `mkdir -p work/step2 && echo OK`
- `cat missing || echo failed`

## 07 Environment and Variables

- `echo "$HOME"; echo "$PATH"`
- `export PATH="$PATH:$(pwd)/scripts"`
- `DATA_DIR="$(pwd)/data"; find "$DATA_DIR" -type f -name '*.csv'`
- `export DATA_DIR; bash -c 'echo "$DATA_DIR"'`
- `(cd "$HOME" && EchoScript.sh)`
