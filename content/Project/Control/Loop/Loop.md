---
title: Open-loop vs Closed-loop
alias: Open-loop vs Closed-loop
---

## Control System

> [!abstract]
> 
> - Mechanism or device that changes the future state or behavior of a system

---

## What is mean by Control

> [!NOTE]
> 
> - More than just changing the state,<br>it means making the **output of the system**<sup>(result)</sup> point towards a **certain desired state**<sup>(goal state)</sup>
> 
> <div align='center'>
> 
>   ```mermaid
> 
>       flowchart LR
>           A[ What I want ]
>           Input --> System --> Output --> A
> 
>   ```
> 
> </div>

---

## Control Theory

> [!important]
> 
> - Branch of mathematics concerned with **strategies for selecting appropriate inputs** to obtain a desired output.
>
>     -> In other words, it deals with **how do I change the input to get what I want?**

> [!tip]
> 
> - Without control theory, you have to find the right inputs through trial and error

---

## Basic Component

> [!abstract]
> 
> > All **control systems** are basically composed of **two parts**
> 
> - When an input acts on a plant, the plant reacts over time to produce an **Output**.
> 
> > [!info]- Plant
> > 
> > - The system under control itself
> >   - **e.g.** dishwasher, lawn, car
> 
> > [!info]- Input
> > 
> > - Signals to the plant

- #### [[./Open.md|Open-loop]]

- #### [[./Closed.md|Closed-loop]]
