---
title: Linux Package Repository
alias: Linux Package Repository
---

> Package tools allow us to download the software we want
 
- **Usage**

  ```bash
  sudo apt install {package name}
  ```

> [!CAUTION]
> 
> - Package repository management is a critical aspect of using open source-based Linux systems.
> - Broken package repository may require a reinstallation of your Linux system

---

### How

> [!NOTE]
> 
> - Fetches the required packages from a specific address on the internet so they can be installed
> - It has Metadata, which contains information about the package (name, version number, package description, etc.).
> - This way, you can always use the packages tool to see what packages your repository has.

---

### Linux Package Repository

> [!abstract]
> 
> - Linux saves package repository sites to a specific file
> 
> > [!info]- Debian
> >
> > > `/etc/apt/source.list`
> >
> > - **Usage**
> > 
> >   ```bash
> >   apt list
> >   ```

---

### source.list

> [!NOTE] Description
> 
> ```bash
> [deb or deb-src] [repository url] [distribution] [component] 
> ```
> 
> > [!info]- deb / deb-src
> >
> > - Binary Package Repositories / Source Package Repositories
> 
> > [!info]- repository url
> > 
> > - The address of that repository
> 
> > [!info]- distribution
> > 
> > - Name of the Linux Version releasing
> 
> > [!info]- component
> > 
> > - **main**
> >   - Free, open-source software that comes standard
> > 
> > <p></p>
> > 
> > - **restricted**
> >   - Officially supported proprietary software
> > 
> > <p></p>
> > 
> > - **universe**
> >   - Open source software maintained & supported by the community
> > 
> > <p></p>
> > 
> > - **multiverse**
> >   - Proprietary software that is not officially supported

---

### Linux Package Installation Process

![[../../../Media/Package_Management.png]]
