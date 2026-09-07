# Linux Navigation & Essential Commands Guide

---

## Part 1: File Systems, Paths & Navigation

### 1. Introduction to File Systems
A **File System** is a structured storage architecture used by operating systems to store, organize, manage, and retrieve data efficiently. Without a file system, storage drives would exist as raw, unorganized pools of bits, making locating, reading, or modifying data practically impossible.

### 2. Directories and Organization
To maintain order, the file system organizes data into **Directories** (folders). 
- Directories act as containers.
- Directories can contain files as well as sub-directories, creating a **nested hierarchy**.

**The Nested Box Analogy:**
### 3. The Root Directory (`/`)
In Linux, the top-most starting point is the **Root Directory**, represented by a single forward slash (`/`).
- It is the ultimate ancestor for every directory and file on the system.
- *Note:* Do not confuse the root directory (`/`) with the **root user** (the administrative superuser account).

### 4. Paths & Navigation
A **Path** is the address used to locate a file or directory.

* **Absolute Path:** Starts from the root directory (`/`) and gives the complete address regardless of your current location.
  * Example: `/home/hacker/projects/program.c`
* **Relative Path:** Interpreted relative to your **Current Working Directory (CWD)**. Does *not* start with `/`.
  * Example: `projects/program.c` (if CWD is `/home/hacker`)

### 5. Special Path Notation Shortcuts

| Symbol | Name | Meaning | Example |
| :---: | :--- | :--- | :--- |
| `/` | Root / Separator | The top directory or path component separator | `cd /` |
| `.` | Current Directory | Refers to your active working directory | `ls .` or `./run` |
| `..` | Parent Directory | Refers to the directory one level up | `cd ..` |
| `~` | Home Directory | Shortcut for the current user's home directory (`/home/hacker`) | `cd ~` or `cd ~/projects` |

* **Executing with `./`:** Linux does not search the current directory for executables by default due to safety precautions. Prepending `./` explicitly runs a program located in the active directory (e.g., `./run`).
* **Tilde (`~`) Expansion:** Bash automatically expands a leading `~` into the full home directory path (e.g., `~/file` expands to `/home/hacker/file`) before executing the command.

---

## Part 2: Essential Linux Commands

### 1. File Reading & Searching

#### `cat` (Concatenate)
Reads and displays the contents of one or more files.
* **Read a single file:** `cat /path/to/file`
* **Concatenate multiple files:** `cat file1 file2`
* **Interactive mode:** Running `cat` with no arguments reads directly from terminal input.

#### `grep` (Global Regular Expression Print)
Searches files for lines matching a specific pattern.
* **Usage:** `grep "SEARCH_STRING" /path/to/file`
* **Example:** `grep "pwn.college" /challenge/data.txt`

### 2. File Comparison & Discovery

#### `diff` (Difference)
Compares two files line by line and highlights differences.
* **Usage:** `diff file1 file2`
* **Understanding output:**
  * `<` indicates lines from `file1`.
  * `>` indicates lines from `file2`.
  * `2c2` means line 2 was changed; `1a2` means line 2 of `file2` was added after line 1.

#### `ls` (List)
Lists directory contents.
* **List current directory:** `ls`
* **List specific directory:** `ls /challenge`
* **Include hidden files (`-a`):** `ls -a /` (reveals files starting with a dot, e.g., `.hidden_file`).

#### `find`
Recursively searches the filesystem hierarchy for files matching criteria.
* **Search by filename across system:** `find / -name "flag"`
* **Search in a target directory:** `find /tmp -name "pwnfile"`

### 3. File & Directory Management

#### `touch`
Creates a new empty file (or updates timestamps).
* **Usage:** `touch /tmp/pwn`

#### `mkdir` (Make Directory)
Creates a new directory.
* **Usage:** `mkdir /tmp/pwn`

#### `rm` (Remove)
Deletes a file permanently.
* **Usage:** `rm delete_me`

#### `mv` (Move / Rename)
Moves or renames a file/directory.
* **Usage:** `mv /flag /tmp/hack-the-planet`

#### `cp` (Copy)
Duplicates a file to a new target path.
* **Usage:** `cp /flag /tmp/hack-the-planet`

### 4. Symbolic Links (Symlinks)

#### `ln -s` (Create Soft Link)
Creates a symbolic link (shortcut) pointing to another file.
* **Syntax:** `ln -s TARGET LINK_NAME`
* **Example:** `ln -s /flag /home/hacker/not-the-flag`

#### `file`
Identifies file types and properties (useful for checking if a file is a symlink).
* **Usage:** `file /home/hacker/not-the-flag`

---

## Part 3: Mental Model & Quick Reference

### Command Quick Reference

| Command | Basic Syntax | Description |
| :--- | :--- | :--- |
| **`pwd`** | `pwd` | Print current working directory |
| **`cd`** | `cd <path>` | Change active directory (`cd` alone goes home) |
| **`ls`** | `ls -a <dir>` | List directory contents (including hidden files) |
| **`cat`** | `cat <file>` | Display file contents |
| **`grep`** | `grep "text" <file>` | Search for matching lines in a file |
| **`diff`** | `diff <file1> <file2>` | Compare differences between two files |
| **`find`** | `find <dir> -name <name>` | Search directory hierarchy for matching files |
| **`touch`** | `touch <file>` | Create an empty file |
| **`mkdir`** | `mkdir <dir>` | Create a directory |
| **`rm`** | `rm <file>` | Delete a file |
| **`mv`** | `mv <src> <dst>` | Move or rename a file |
| **`cp`** | `cp <src> <dst>` | Copy a file |
| **`ln -s`** | `ln -s <target> <link>` | Create a symbolic link |
| **`file`** | `file <path>` | Identify file type |
| **`./`** | `./program` | Execute a file in the current directory |