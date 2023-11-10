# linux-cheat-sheet
> my public linux cheat sheet containing some commands I might use & a short explanation of each one

---

## Contents List

| Topic                                                                   |
| ----------------------------------------------------------------------- |
| [**Basic commands**](#basic-commands)                                   |

## Basic commands
> [**Basic commands notes**](#basic-commands-notes)

| Command                      |
| ---------------------------- |
| **pwd**                      |
| **ls**                       |
| **history**                  |
| **mkdir -p**                 |
| **rmdir**                    |
| **cat**                      |

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

4. **mkdir -p** creates parent directories recursively

```bash
   $ mkdir -p d/inside-d
   $ ls -R
   .:
   d

   ./d:
   inside-d

   ./d/inside-d:
```

5. **rmdir** removes empty directories

```bash
   $ rmdir <directory1 name> <directory2 name> ...
```

we can force it to remove non-empty directories but it's more common to use rm -rf instead

rmdir -p: removes parent directories recursively
```bash
   $ rmdir -p d/inside-d/inside-inside-d
```

6. **cat** shows file's contents

```bash
   $ cat a.txt
   nothing special here

   -n : if you add this option, it shows files line numbers too
```

we can use this command to add to a file(using the option below everything we type will be saved in a.txt):
```bash
   $ cat > a.txt
```

### Basic commands notes

1. **~** denotes a user's home directory

```bash
   $ cd ~
   $ pwd
   /home/mobin
   ```