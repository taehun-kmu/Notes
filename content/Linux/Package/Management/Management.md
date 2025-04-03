---
title: Linux Package Management System
alias: Linux Package Management System
---

- Using the **Package Management Tool** to manage packages

---

### Low Level Package Tool

> [!abstract]
> 
> > Tools for installing or removing package files
> 
> - You can install and uninstall files from each package,<br>but you don't know the dependencies between packages.

> [!info]
> 
> - **Debian** : `dpkg`
> - **Red Hat** : `rpm`

---

### High Level  Package Tool

> [!abstract]
> 
> > Tools to install and uninstall package files,<br>as well as search for downloadable packages and resolve Package Dependencies.
> 
> - Resolving package dependencies means that the package will identify any dependencies between packages<br>it has and automatically install them if necessary.

> [!info]
> 
> - **Debian** : `apt-get`, `apt`, `aptitude`, `nala`
> - **Red Hat** : `yum`. `dnf`
