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
   -a : show everything including hidden
   -R : goes into every directory and recursively lists
   -h : shows memory section human readable (should be used with -l)
```


### Basic commands notes

1. **~** denotes a user's home directory

```bash
   $ cd ~
   $ pwd
   /home/mobin
   ```