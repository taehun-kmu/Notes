---
title: Secure SHell
alias: Linux Secure SHell
---

> [!abstract]
> 
> - **Protocol** that allows you to access or run commands on **another computer over a network**.
> - This means you can **access Linux from another computer** via SSH to **Run commands** & **Programs**

> [!NOTE]
> 
> - On **Ubuntu**, you can run SSH through a **package** called `openssh`
> - After installing **Ubuntu**, only `openssh-client` is installed by **default**
> - To access **Ubuntu** from **another computer**, you need to install the `openssh-server` **package**

> [!tip]
> 
> - You can check if **openssh** is installed by running the command `dpkg -l | grep openssh`
> - Can be installed via `sudo apt-get install open-ssh-server`

---

### Run the Server

> [!cite]
> 
> ```bash
> sudo service ssh start
> service --status-all | grep +
> ```
> 
> - Enter `stop` instead of `start` for shutdown and `restart` for restart
> - If you only want to see **ssh**, type `service --status-all | grep ssh`

### Check the Port

> [!cite]
> 
> - To use **SSH**, another computer needs to know what **Port** to connect to your computer on
> - You can check the **Port** of the **SSH** you're running on with the `sudo netstat -antp`
> - You can see the currently running processes and **Ports** along with their [[../Process/Characteristic.md|PID]]

### Connect to a Port

> [!cite]
> 
> - `ssh [server-id] @[IP || server-name || domain` to connect to that **server**
