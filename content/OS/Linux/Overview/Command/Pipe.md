---
title: Pipe
alias: Linux Command Pipe
---

- Similar to **file redirection**, **pipe separates** commands with `|`

- Can write multiple complex instructions in parallel

---

> [!example]
> 
> 1. Output the contents of `{file1}`
> 2. Run `{file2}.py` with the output
> 3. Write that to `{file3}` -> Use to [[./Redirection.md|File Redirection]]
>
> > [!check]-
> > 
> > <code>cat {file1} | {file2}.py >> {file3}</code>
> 
