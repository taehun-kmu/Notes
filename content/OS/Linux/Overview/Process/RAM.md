---
title: Configuring RAM(Memory)
alias: Linux Process Configuring RAM(Memory)
---

<div style='display: flex; justify-content: space-around; align-items: center;'>
  <div align="center">

  ```mermaid

  flowchart TD
      A[ Code Area ]
      B[ Data Area ]
      C[ BSS Area ]
      D[ Hip Area ]
      E[ &vellip; ]
      F[ Stack Area ]
      G[ Kernel ]

      A --> B --> C --> D --> E --> F --> G

  ```

  </div>
  <div>

  > [!info]- Code Area
  > 
  > > **Program Code**(bottom)

  > [!info]- Data Area
  > 
  > > **Initialized variable**
  > > - Global & static variable, array structs, etc.

  > [!info]- BSS Area
  > 
  > > **Uninitialized variable**
  > > - Created when the program runs, returned after exit

  > [!info]- Hip Area
  > 
  > > **Dynamically assigned variable**

  > [!info]- User Area
  > 
  > > Where libraries are stored

  > [!info]- Stack Area
  > 
  > > **Areas that programs use automatically**
  > > - Store temporary material such as function parameters, return addresses, and local variables.
  > > - Remove after function end(LIFO)

  </div>
</div>

---

> [!important] Process Memory
> 
> - Can be broadly separated into **kernel space** & **user address space**
> - The kernel part is **Not Accessible** to users
> 
> > [!info]- User Adress Space
> > 
> > - **Stack**
> > - **Heap**
> > - **Data**
> > - **Text**
> > 
> > > The `argv`, `argc`, `env`, `etc` files are also part of the **stack**.
