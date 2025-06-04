---
title: Basic Shell Command
alias: Linux Shell Basic Command
---

> [!todo]- cd
> 
> - Short for **change directory**, used when you want to go to a specific directory.
> 
> ```bash
> cd {Path to the Directory}
> 
> cd    # User Directory
> cd    # root Directory
> cd    # Parent Directory
> 
> cd Desktop/Workspace     # Navigate to the Desktop subdirectory Workspace
> ```

> [!todo]- ls
> 
> - Short for **list**, it lists the files and directories in the current directory.
> 
> ```bash
> ls     # Print the contents of the current directory
> {Directory1}  {Directory2}  {Directory3}
> ```
> 
> ```bash
> ls -a     # Show hidden files or directories as well
> .{Directory1}  {Directory2}  {Directory3}
> .{Directory4}  {Directory5}
> ```
> 
> ```bash
> ls -l     # Details (permissions, number of files included, owner, group, file size, modification date, filename)
> {Permission}  {Number of Hard link}  {USER}  {Group}  {Size}  {Month}  {Day}  {Time}  {Name of the File or Directory}
> ```
> 
> ```bash
> ls -al
> total {Number}
> {Permission}  {Number of Hard link}  {USER}  {Group}  {Size}  {Month}  {Day}  {Time}  {Name of the File or Directory}
> ```
> 
> ```bash
> ls -h -al     # -h to use file sizes in K, M, and G to make them human-readable
> total {Number}
> {Permission}  {Number of Hard link}  {USER}  {Group}  {Size}  {Month}  {Day}  {Time}  {Name of the File or Directory}
> ```

> [!todo]- mv
> 
> - Short for **move** and can be used to move or rename a file or directory to where you want it to go
> 
> ```bash
> # Move Files to that directory
> mv {Origin Filename} {Name of the directory you want to move}
> ```
> 
> ```bash
> # Rename the file
> mv {Origin Filename} {Filename you want to rename}
> ```
> 
> ```bash
> # Move directories to that directory
> mv {Origin Directory} {Name of the directory you want to move}
> ```
> 
> ```bash
> # Rename the directory
> mv {Origin Directory} {Directory you want to rename}
> ```

> [!todo]- cp
> 
> - Short for **copy**, which allows you to copy a file or directory anywhere you want, with any name you like
> 
> ```bash
> # Copy files to that directory
> cp {Origin Filename} {Name of the directory you want to move}
> ```
> 
> ```bash
> # Create a copy file with that filename
> cp {Origin Filename} {Filename you want to copy & create}
> ```
> 
> ```bash
> # Copy multiple files to a directory at once
> cp {Origin FIlename1} {Origin Filename2} {Name of the directory you want to move}
> ```
> 
> ```bash
> # Copy all subfiles of the source directory to that directory, even the subfiles of the source directory
> cp {Origin Directory} -r {Name of the directory you want to move}
> ```
> 
> ```bash
> # Create the directory you want to copy and create using the above method
> cp {Origin Directory} -r {Filename you want to copy & create}
> ```

> [!todo]- cat
> 
> - Short for **concatenate**, used to concatenate two or more files for output.
> 
> ```bash
> # Usage
> cat {file1} {file2} ...
> Content1
> Content2
> ```
> 
> ```bash
> # Output with a line preceding the result
> cat -n  {file1} {file2}
> 1 {Content1}
> 2 {Content2}
> ```
> 
> ```bash
> # Combines the contents of files preceded by ">" into a new file
> cat {file1} {file2} ... > {new file}
> ```
> 
> ```bash
> # Combine the contents of files preceded by ">" to overwrite existing files
> cat {file1} {file2} ... > {Existing file}
> ```
> 
> ```bash
> # Combine the contents of files before the ">" and append them after the existing file
> cat {file1} {file2} ... >> {Existing file}
> ```

> [!todo]- less
> 
> - One of the commands to check the contents of a file
> - Write new output to an internal window, like vim, only as much as is visible at a time
> 
> ```bash
> less {file}
> ```
> 
> > [!check]
> > 
> > - `q` : Return to the shell window after exiting
> > - `enter` : Move down 1 row
> > - `space bar or f` : Go down 1 page
> > - `number+n` : Go back as many pages as you want
> > - `PageUp` : Go up 1 page
> > - `PageDown` : Go down 1 page

> [!todo]- tail
> 
> - Prints a portion of the file's contents up to the specified line, based on the last line of the file.
> 
> ```bash
> # basic
> # Output the last 10 rows of the text file entered from 1 to {Last Number}
> tail {filename}
> ```
>
> ```bash
> # The rows from the last row to the corresponding
> tail -n {Number} {filename}
> ```
> 
> ```bash
> # Output from that row to the last row
> tail +{Number} {filename}
> ```
> 
> ```bash
> # Output by byte instead of by row
> tail -c {Number} {filename}
> ```
> 
> ```bash
> # Output the last 10 lines in real time without exiting
> # Exit with CTRL+C
> tail -f {filename}
> ```

> [!todo]- mkdir
> 
> - Short for **make directory**, which allows you to create a new directory
> - `touch {filename}` can create a new file
> 
> ```bash
> # Create a new directory at that path
> mkdir {New Directory}
> ```
> 
> ```bash
> # Create subdirectories together
> mkdir -p {New Directory +"/" + New subdirectory name}
> ```

> [!todo]- clear
> 
> - Clear all history in the shell window
> 
> ```bash
> clear
> ```

> [!todo]- pwd
> 
> - Short for **print working directory**, returns the absolute path to the directory you are currently working in
> 
> ```bash
> pwd
> {Path}
> ```

> [!todo]- chown
> 
> - Change the owner and group identifier of a file or directory
> 
> ```bash
> # Change the file's owner, group identifier, or name
> chown {Owner}:{Group} {Filename you want to change ownership of}
> ```
> 
> ```bash
> # Change the owner, group identifier for that directory (but not subdirectories)
> chown {Owner}:{Group} {Name of the directory you want to change ownership of}
> ```
> 
> ```bash
> # Changing the owner, group identifier, and ownership of the directory and its subdirectories
> chown -R {Owner}:{Group} {Filename you want to change ownership of}
> ```

> [!todo]- chmod
> 
> - Commands that allow you to modify the permissions for a file or directory
> 
> ```bash
> chmod {Permission value to be changed} {Files/directories to change}
> ```
> 
> ```bash
> chmod {Number} {File/directories to change}
> ```

> [!todo]- grep
> 
> - Finds strings with a specified pattern within a specific file and prints them out
> - Use patterns in regular expressions for patterns
> 
> ```bash
> # Output a string with a specific pattern from a specific file
> grep {Pattern} {filename}
> ```
> 
> ```bash
> # Output a string with a specific pattern from all files in the current directory
> grep {Pattern} *
> ```
> 
> ```bash
> # Output strings with a specific pattern in the current directory and subdirectories
> grep {Pattern} * -r
> ```

> [!todo]- history
> 
> - Output a list of all the commands you've hit so far, with line numbers
> 
> ```bash
> history
> 1 history
> 2 cd
> 3 ls
> ...
> ```
> 
> ```bash
> # Clearing the history list
> history -c
> ```

> [!todo]- ps
> 
> - Output a list of currently working processes
> 
> > [!check]
> > 
> > - `-a` : Process output for all users
> > - `-u` : Output each process user and usage time
> > - `-x` : Process output without a control terminal
> > - `-l` : Output detailed forms of information
> > - `-e` : Output all process statuses
>
> ```bash
> # Output all processes on the system using BSD syntax
> ps -aux 
> ```
> 
> ```bash
> # Outputting processes as a tree
> ps -ejH
> ```

> [!todo]- man & tldr
> 
> - `man` prints something that explains how the command is written
> - However, it's a little bit too much to read, so I use `tldr` instead, which only tell you the important parts.
> 
> ```bash
> man ls
> NAME
>     ls --list directories contents
> 
> SYNOPSIS
>     ls [-ABCFGHLOPRSTUW@abcdefghiklmnopqrstuwx1%] [file ...]
> 
> DESCRIPTION
>     For each operand that names a file of a type other than directory, ls displays its name as well as any requested, associated information.  For each operand
>     that names a file of type directory, ls displays the names of files contained within that directory, as well as any requested, associated information.
> 
>     If no operands are given, the contents of the current directory are displayed.  If more than one operand is given, non-directory operands are displayed
>     first; directory and non-directory operands are sorted separately and in lexicographical order.
> 
>     The following options are available:
> 
>     -@      Display extended attribute keys and sizes in long (-l) output.
> 
>     -1      (The numeric digit ``one''.)  Force output to be one entry per line.  This is the default when output is not to a terminal.
> 
>     -A      List all entries except for . and ...  Always set for the super-user.
> > 
>     -a      Include directory entries whose names begin with a dot (.).
> 
>     -B      Force printing of non-printable characters (as defined by ctype(3) and current locale settings) in file names as \xxx, where xxx is the numeric
>             value of the character in octal.
> 
>     -b      As -B, but use C escape codes whenever possible.
> 
>     -C      Force multi-column output; this is the default when output is to a terminal.
> 
>     -c      Use time when file status was last changed for sorting (-t) or long printing (-l).
> 
>     -d      Directories are listed as plain files (not searched recursively).
> 
>     -e      Print the Access Control List (ACL) associated with the file, if present, in long (-l) output.
> 
>     -F      Display a slash (`/') immediately after each pathname that is a directory, an asterisk (`*') after each that is executable, an at sign (`@') after
>             each symbolic link, an equals sign (`=') after each socket, a percent sign (`%') after each whiteout, and a vertical bar (`|') after each that is a FIFO.
> ```
> 
> ```bash
> tldr ls 
> ls
> 
> List directory contents.
> 
> - List files one per line:
>     ls -1
> 
> - List all files, including hidden files:
>     ls -a
> 
> - Long format list (permissions, ownership, size and modification date) of all files:
>     ls -la
> 
> - Long format list with size displayed using human readable units (KB, MB, GB):
>     ls -lh
> 
> - Long format list sorted by size (descending):
>     ls -lS
> 
> - Long format list of all files, sorted by modification date (oldest first):
>     ls -ltr
> ```

---

### Tip

- `Control + a` : Cursor moves to the beginning of the line
- `Control + e` : Cursor moves to the end of the line
