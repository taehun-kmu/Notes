---
title: Process Characteristics
alias: Linux Process Characteristic
---

1. Every program has **One or more Processes** when it runs
2. Can run in **parallel**
3. You now have a **parent**(PPID), **child**(copied via fork) process
4. Managed by the **kernel**
5. Every process has an **Owner**(Linux account)
6. Each process is given an **identifier**(PID) **for identification**.

---

> [!important] PID
> 
> > Every process has a **unique PID**
> 
> 1. Run to `init Process`
> 2. Run to `kthreadd(kernel thread demon) Process`
> 
> > [!info] init Process
> > 
> > - The **parent process** of all remaining system processes,<br>all non-`kthreadd` processes **created by forking** the `init process`
> 
> > [!info] kthreadd
> > 
> > - **Parent process of all processes that run after this**
