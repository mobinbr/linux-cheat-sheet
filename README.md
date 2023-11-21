# linux-cheat-sheet
> my public linux cheat sheet containing some commands I might use & a short explanation of each one

---

## Contents List

| Topic                                                 |
| ----------------------------------------------------- |
| [**Basic commands**](#basic-commands)                 |
| [**File and strings**](#file-and-strings)             |

## Basic commands
> [**Basic commands notes**](#basic-commands-notes)

| Command          |
| ---------------- |
| **pwd**          |
| **ls**           |
| **history**      |
| **mkdir -p**     |
| **rmdir**        |
| **cat**          |
| **cp**           |
| **mv**           |
| **rm**           |

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
   mkdir -p [new directory name]/[the insider directory name inside the new directory]
```
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
   $ rmdir [directory1 name] [directory2 name] ...
```

we can force it to remove non-empty directories but it's more common to use rm -rf instead

rmdir -p: removes parent directories recursively
```bash
   $ rmdir -p d/inside-d/inside-inside-d
```

6. **cat** shows file's contents

```bash
   cat [file name]
```
```bash
   $ cat a.txt
   nothing special here

   -n : if you add this option, it shows files line numbers too
```

we can use this command to add to a file(using the option below everything we type will be saved in a.txt):
```bash
   $ cat > a.txt
```

7. **cp** copies file or directory to a destination path

copy file:

```bash
   cp [file you want to copy] [the path you want your file to be copied to and the name of it]
```

make a copy of a.txt in mydir named b.txt
```bash
   $ cp a.txt mydir/b.txt
```

copy directory:

we use -r option to copy directories along with their contents

```bash
   cp -r [directory you want to copy]/ [the path you want your directory to be copied to and the name of it]
```

make a copy of mydir1 to pdir named mydir2
```bash
   $ cp -r mydir1/ pdir/mydir2
```

8. **mv** cuts file or directory to a destination path, rename a file or directory

move file:

move a.txt to mydir directory
```bash
   $ mv a.txt mydir/
```

move directory:

move mydir1 directory to mydir2 directory
```bash
   $ mv mydir1/ mydir2/
```

rename:

rename a.txt to b.txt
```bash
   $ mv a.txt b.txt
```

9. **rm** removes file or directory

remove a.txt
```bash
   $ rm a.txt
```

remove a directory
```bash
   $ rm -r mydir/
```

### Basic commands notes

1. **~** denotes a user's home directory

```bash
   $ cd ~
   $ pwd
   /home/mobin
   ```

2. use **--help** or **man** to get description of the command you need

3. there are 3 types of standard streams:
 - standard input stream: source of input for the program
 - standard output stream: used for output from the program
 - standard error stream: used for error messages 

4. pipelines are a kind of redirection in which we use to connect commands and get output from one and give it as input to another

```bash
   $ cat <<EOF | sort
   hello
   from
   alireza
   in quera
   to
   you
   EOF

   alireza
   from
   hello
   in quera
   to
   you
```

## File and strings
> [**File and strings notes**](#file-and-strings-notes)

| Command       |
| ------------- |
| **du**        |
| **file**      |
| **find**      |


1. **du** shows the space usage of files and directories of the current directory 

```bash
   $ du
   680	    ./HWs/HW1
   680	    ./HWs
   32752	./slides/microcontroller_AVR
   16536	./slides/microprocessor
   49288	./slides
   230656   ./voices
   280624	.
```
as you can see, it recursively shows each directories space usage

we can pass the address to du too

there are some usefull options too:
```bash
   options:
   -h : shows space usage human readable
   -sh : just shows current direcotiry
```

2. **file** shows files type

```bash
   file [file name]
```
```bash
   $ file README.md
   README.md: ASCII text
```

3. **find** finds files and directories

```bash
   $ find [starting directory to search] -name "[file to search]"
```
```bash
   find . -name "*.txt"
```

4. **

### File and strings notes

1. there are several editors in linux like vim & nano
```bash
   $ nano a.txt

   $ vim a.txt
```
