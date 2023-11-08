# linux-cheat-sheet
> my public linux cheat sheet containing some commands I might use & a short explanation of each one

---

## Contents List

| Topic                                                                   |
| ----------------------------------------------------------------------- |
| [**Basic commands**](#basic-commands)                                   |

## Basic commands
> [**Basic commands notes**](#basic_commands_notes)

1. **pwd** shows your current directory

```bash
   $ pwd
   /home/mobin
   ```

2. **ls** lists files and directories

```bash
   $ ls
   HW  slides
   ```

there are different options for ls command:

```bash
   -t : sort by last modified (newest first)
   -l : more detailed
   $ ls -l
   total 4
   drwxrwxrwx 1 mobin mobin    0 Oct 11 16:41 HW
   drwxrwxrwx 1 mobin mobin 4096 Sep 30 10:14 slides

   -a : show everything including hidden
   -R : goes into every directory and recursively lists
   -h : shows memory section human readable (should be used with -l)
```

3. **history** shows previously executed commands

```bash
   $ history
   ...
   2203  ls
   2204  ls -l
   2205  history
   2206  pwd
```

### Basic commands notes

1. **~** denotes a user's home directory

```bash
   $ cd ~
   $ pwd
   /home/mobin
   ```