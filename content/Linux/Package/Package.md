---
title: Linux Package
alias: Linux Package
---

## Introduction

> [!abstract]
> 
> - Downloaded a zipped file or downloaded a file to help you install, like the Windows installer
> - On Linux, these files are collectively known as **Packages**.

---

## Package

> A bundle of installation files that contains the files needed to run the software<br>on a Linux system (executables, configuration files, libraries, etc.)

- #### [[./Source.md|Source Package]]
- #### [[./Binary.md|Binary Package]]

---

## Packaging System

- Different Linux distributions have different ways of packaging, but there are two main ones

> [!info]- Debian
> 
> > **DEB**(`.deb`)
> 
> - Debian, Ubuntu, Linux Mint, etc

> [!info]- Red Hat
> 
> > **RPM**(`.rpm`)
> 
> - Red Hat, Fedora, Cent OS, etc

---

### Management System

> Using the **Package Management Tool** to manage packages

- #### [[./Management/Low.md|Low Level Package Tool]]

- #### [[./Management/High.md|High Level Package Tool]]

---

### Package Repository

> [!NOTE]-
> 
> - Package tools allow us to download the software we want
> 
> ```bash
> sudo apt install {package name}
> ```

> [!abstract]-
> 
> - Fetches the required packages from a specific address on the internet so they can be installed
> - It has Metadata, which contains information about the package (name, version number, package description, etc.).
> - This way, you can always use the packages tool to see what packages your repository has.
> 
> ```bash
> apt list
> ```
> 
> > [!info]
> > 
> > > Linux saves package repository sites to a specific file
> > 
> > - **Debian** : `/etc/apt/source.list`
