---
title: Schedule Task
alias: Linux Schedule Task
---

### at

> [!abstract]
> 
> **Scheduled Task command** that runs once at a specified time, performs when it's time, and disappears from the **task list**.

> [!check]
> 
> `at {Option} {Time} {Date} {+ Incremental Time}`
> 
> - `-m` : Send a mail to the user when the task completes with the output (even if there are no results)
> - `-f` : Used to run specific script files, etc.
>   - **Ex.** `at now + 3 hours -f {Shell Script}`
> - `-l` : Outputs a list of scheduled tasks, performing the same behavior as the `atq`[^1]
> - `-v` : Output the exact time the action will be performed
> - `-d` : Deletes a scheduled task, performing the same behavior as the `atrm`[^2]

---

### crontab

> [!abstract]
> 
> Unlike `at`, `crontab` can run periodic schedules

> [!check]
> 
> `crontab {Option} {Text for Option}`
> 
> - `-l` : Shows set `crontab` information for the current account
> - `-e` : Modify `crontab` information for the current account
> - `-r` : Delete all `crontab` information for the current account
> - `-u` : Allows you to manipulate `crontab` information for a specific user, requires **root privileges**, used with `sudo`


[^1]: `atq` : Shows a list of ATs that are scheduled to run (atnumber date time command)
[^2]: `atrm {at Number}` : Delete that reservation
