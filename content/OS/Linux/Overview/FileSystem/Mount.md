---
title: Mount
alias: Linx Mount
---

- Linking **physical storage devices**(secondary memory) to **directories**(folders)

- Windows **automatically connects** to directories (folders) when you connect a **secondary memory device**(hard, USB, etc.)

> [!info]- PnP
> 
> - It will be ready to use as soon as you plug in the **USB**, which is called **Plug and Play**
> 
> > [!CAUTION]
> > 
> > - PnP feature does **not work** on Linux
> > - Must perform a mount operation when installing a secondary memory for direct connection
> 

---

### Command

> [!Note] Default Form
> 
> > `mount {Option} {Device} {Directory}`
> 
> - Linking the contents of a **Device** to a **Directory**
> - You need to know the **file system name** of the **device**, which can be found with `fdisk -l`

> [!info] Options
> 
> - `-a` : Used to **mount filesystems** specified in `etc`/`fstab`
> - `-t` : Used to specify a non `etx`/`fstab` **file system type**
> - `-o` : Used when **additional settings** are required, and separated by `,` when **applying multiple conditions**.
> 

> [!tip]
> 
> - Print mounted **disk information**
>   - `df`
> 
> <p></p>
> 
> - **Unmount**
>   - `remount {Device} {Directory}`
