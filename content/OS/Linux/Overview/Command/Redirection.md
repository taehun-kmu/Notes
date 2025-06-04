---
title: File Redirection
alias: Linux File Redirection
---

- Reversing the flow of a standard stream, which means redirecting it to a different path,<br>a file, rather than using the usual **standard streams**(standard input and output and error).

<p></p>

- Can be used with `<` & `>`

---

> [!info] Standard Steam
> 
> - **stdin** : Standard input-keyboard input
> - **stdout** : Standard Output-Screen Output (`cat`, `ls`)
> - **stderr** : Standard error output

> [!example]
> 
> - If you type `ls > exitedFilename.txt`,<br>the result of the `ls` command is saved to `exitedFilename.txt` instead of being printed to the console.
>  
> > [!CAUTION]
> > 
> > - Replaces existing content
> 
> - If the file does not exist, use `>>` instead, for example, `ls >> newFilename.txt`
> - If `newFilename.txt` already exists, we don't erase the existing contents, but instead write it after the last line
