# Shell

The terminal is the “window” (more or less), while the shell is a program (or a programming language, like R and Python are). The shell has been around longer than most of its users have been alive. It has survived because it’s a powerful tool that allows users to perform complex and powerful tasks, often with just a few keystrokes or lines of code. It helps users automate repetitive tasks and easily combine smaller tasks into larger, more powerful workflows. There are several shell programs, `bash` (and `zsh`) being the most common. They are almost equivalent. For Window users, `PowerShell` is the command shell and scripting language. 

After you have a terminal open, type `echo $SHELL`. You may see this:

```
> echo $SHELL
/bin/bash
```

# Summary

- Shell References: [2. navigating files and directories](https://swcarpentry.github.io/shell-novice/02-filedir/index.html) and [3. working with files and directories](https://swcarpentry.github.io/shell-novice/03-create/index.html) from [software carpentry introduction](https://swcarpentry.github.io/shell-novice/). 

- directory structure, root is `/`
- relative versus absolute paths
   - in your code and projects: use relative paths as much as possible: it makes your code more portable, for others, and for yourself if you re-locate your own project folder
- shortcuts: `.`, `..`, `~`, -`
- `cd -` is so useful!
- tab completion to get program and file names
- up/down arrows and `!` to repeat command


| Command 	| Task 	| Quiz
| ---	|---	| :---: 
| `whoami` | who am I? to get your username | O
| `echo` |  print | O
| `pwd` |  print working directory. where am I? | O
| `ls` | list. many options, e.g. `-a` (all) `-l` (long) `-lrt` (reverse-sorted by time) | O
| `cd` | change directory | O
| `mkdir` | make directory | O
| `rm` | remove (forever). `-f` to force, `-i` to ask interactively, `-r` recursively | O
| `rmdir` | remove (delete) directory, if empty | O
| `mv` | move (and rename). can overwrite existing files, unless `-i` to ask | O
| `cp` | copy. would also overwrite existing files | O
| `touch` | create blank file, or modify time stamp of existing file | 
| `nano` | run a text editor called Nano to create/modify a file |
| `diff` | difference
| `wc` | word count: lines, words, characters. `-l`, `-w`, `-c`
| `cat` | concatenate
| `less` | because “less is more”. `q` to quit.
| `sort` | `-n` for numerical sorting.
| `head` |  first 10 lines. `-n 3` for first 3 lines (etc.)
| `tail` |  last 10 lines. `-n 3` for last 3 lines, `-n +30` for line 30 and up
| `uniq` | filters out repeated lines (consecutive). `-c` to get counts 
| `cut` | cut and return column(s). `-d`, to set the comma as field delimiter (tab otherwise), `-f2` to get 2nd field (column) 
| `history` |  shows the history of all previous commands, numbered
|  `!` |  `!76` to re-execute command number 76 in the history, !$ for last word or last command

# File names
so important: **no spaces!** example:

- create a directory ‘data science’ in `repos`, using a graphical user interface (GUI; e.g., Finder)
- try to remove it from the command line:

```
cd repos
ls
rm -rf data science
```

lucky for us: `data` or `science` didn’t exist (chainsaw…)

how can we remove this directory?

- prefer lower-case letters, especially for the first letter of a file name: time saver, along with tab completion

- common usage: capitalize between words, or underscores, or `-`, like `shellWarmupActivities` (camel case style) or `shell_warmup_activities` (snake case style).

- use ASCII characters only, no space, no `/`, no `\` (for Windows), no `-` for the first character.

- R users: avoid dots. conventionally used for the file extension.

