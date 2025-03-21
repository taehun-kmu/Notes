---
title: Linux Permissions
---

## Permission Error

```bash
Permission denied.
```

- Current User가 `File에 대한 Permissions이 없어서` 발생하는 Error

## Linux's Permission Scheme

- Linux에서는 각 By File, By User, By Permission type으로 Permission을 Manage

- 각 Permission은 By User(File Owner, Group the Owner, Other Users)에 따라 3bit의 2진수로 부여되고 확인 가능

<table style='max-width: 700px; table-layout: fixed; width: 100%; font-size: 12px; margin-left: auto; margin-right: auto'>
  <tr>
    <th style='text-align: center'><p style='line-height: 1.5'>d<br>&nbsp;</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>r<br><span style='font-weight: normal'>read</span></p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>w<br><span style='font-weight: normal'>write</span></p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>x<br>exec</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>r<br>read</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>&ndash;<br>write</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>x<br>exec</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>r<br>read</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>&ndash;<br>write</p></th>
    <th style='text-align: center'><p style='line-height: 1.5'>&ndash;<br>exec</p></th>
  </tr>
  <tr>
    <td rowspan="3" style='text-align: center'><p style='white-space: nowrap'>File type<br>(directory)</p></td>
    <td colspan="3" style='text-align: center'>Owner permissions</td>
    <td colspan="3" style='text-align: center'>Group permissions</td>
    <td colspan="3" style='text-align: center'>User permissions</td>
  </tr>
  <tr>
    <td style='text-align: center'>4</td>
    <td style='text-align: center'>2</td>
    <td style='text-align: center'>1</td>
    <td style='text-align: center'>4</td>
    <td style='text-align: center'>2</td>
    <td style='text-align: center'>1</td>
    <td style='text-align: center'>4</td>
    <td style='text-align: center'>2</td>
    <td style='text-align: center'>1</td>
  </tr>
  <tr>
    <td colspan="3" style='text-align: center'>7</td>
    <td colspan="3" style='text-align: center'>5</td>
    <td colspan="3" style='text-align: center'>4</td>
  </tr>
</table>

## Super User(root)

> Root can override all Permissions.

- Ex)
  - To log in as a different user, You need to enter that user's password.<br>However, Root can log in as that user without entering a password.
  - Root can read, change, and execute files regardless, even if they have permissions other than owner.

> 그렇기에 `Managing root privileges은` **아주 중요하다.**
> Be careful not to give Root privileges to just anyone.

## Authorization Command(chmod)

- To change the permissions of a file, You can use the chmod command.

### Number

```bash
chmod 755 {filename}    // rwx r-x r-x
chmod 755 {filename}    // rwx r-- r--
```

- This is useful when setting global permissions because you can set all permissions for all users at once.

### Character

```bash
chmod u+w {filename}
chmod g+r {filename}
```

- This is easy if you're setting up some permissions.
  - `u/g/o/a`: user(Owner), group, other, all
  - `+/=/-`: Add, assign, and delete permissions
  - `r/w/x`: Read, write, and execute permissions
