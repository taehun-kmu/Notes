---
title: Linux Process Related Command
alias: Linux Process Related Command
---

> [!check] View the list of processes
> 
> `ps {Option}`
> 
> - `-e` : Output information about all currently running processes
> - `-f` : See all the information
> - `-a` : Output all running processes for all users
> - `-u` : Trace who ran the process and when the process started, etc.
> - `-x` : View process status without terminal control

> [!CAUTION] Ending a process
> 
> `kill {Option} {PID}`
> 
> - `-l` : Output a list of available signals
> - `-1` : Redo(SIGHUP)
> - `-9` : Force Quit(SIGKILL)
> - `-15` : Normal Shutdown(SIGTERM)

---

### job

> [!NOTE]
> 
> > Almost every command that works through the terminal in Linux works in the **foreground**
> 
> - In other words, it works on the screen we're looking at right now.
> - However, you can use the `&` to make it run out of sight with the **background**

---

> [!abstract]
> 
> - Commands that show you what's running in the **background** and let you use it efficiently
> - Unlike a process, it only refers to work via terminal commands, and there is a separate job for each terminal.
> - In other words, when the terminal is terminated, the job is terminated as well.
> 
> <p></p>
> 
> - Adding `&` after the command will run in the **background**, a list of which can be found via `jobs`
> - As with processes, you can also use the `ps` to find out the [[./Characteristic.md|PID]] of a process and kill it.
> - Can also be terminated via `kill %[job number]` without options

> [!example]
> 
> > The process of running and exiting the `sleep` command, **which means pause**, in the **background** is as follows
> 
> ```bash
> sleep 500 &
> sleep 700 &
> 
> jobs
> ```
> 
> - This is the resulting screen
> 
> ```bash
> [1] - Running sleep 500 &
> [2] + Running sleep 700 &
> ```
> 
> - At this point, enter `sleep 500 &` `kill %1` to exit
