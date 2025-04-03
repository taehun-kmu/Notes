---
title: Build System
alias: Linux Build System
---

> [!tip] 
> 
> The **ament build system**, the build system for **ROS**/**ROS2**, also builds internally using **Make**

---

## What are Build & Build System?

> [!abstract]
> 
> - The point of coding is to take the source code you write and create a program that does what you want it to do.
> - To build is to do this process
> - In other words, the act of turning source code into a program is what we call building, and the tools that help us do this are called build systems.
> 
> <div align='center'>
> 
>   ```mermaid
>   
>       flowchart LR
>           A[ Source code ]
>           B[ **Build** ]
>           C[ Executable File ]
> 
>           A --> B --> C
>           
>   ```
> 
> </div>

> [!info]- Build System
> 
> - Includes programs, compilers, linkers, scripts, etc.
> - You don't have to use a specific program to build C/C++ code, but can use it optionally

> [!info]- Build
> 
> - Includes compilation to convert files to machine language and links to link the converted files into a final program.
> 
> <div align='center'>
>
>   ```mermaid
> 
>       flowchart TB
>           subgraph **Build**
>           Compile ~~~ Link
>           end
> 
>   ```
> 
> </div>

- #### [[./Process/Process.md|Process]]
