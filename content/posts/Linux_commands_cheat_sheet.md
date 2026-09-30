---
date: '2026-09-20T00:44:14+08:00'
draft: false
title: 'Linux_commands_cheat_sheet'
tags:
  - Linux
---

## 应用程序管理
#### which

```bash
$ which clear
/usr/bin/clear
```



####  yum

安装和卸载系统中的工具

```bash
$ sudo yum -y install net-tools
```



### 控制台和输出管理
#### cat

文件内容输出

```bash
$ cat /etc/system-release
Red Hat enterprise Linux release 8.5
```



#### echo

```bash
$ echo "hello world"
hello world
```

```bash
echo "hello world" > data.txt
```



#### top

显示有关正在运行的Linux进程的信息

示例：显示top命令，并将结果通过管道符传递给more命令，一边查看输出的第一页

```bash
$ top | more
top - 12:02:29 up 5 days, 20:20, 2 users, load average: 0.01, 0.02, 0.00
Tasks: 201 total, 2 running, 199 sleeping, 0 stopped, 0 zombie
%Cpu(s): 0.0 us, 6.2 sy, 0.0 ni,93.8 id, 0.0 wa, 0.0 hi, 0.0 si, 0.0
st
MiB Mem : 7770.8 total, 5409.8 free, 1240.8 used, 1120.2 buff/cache
MiB Swap: 8092.0 total, 8092.0 free, 0.0 used. 6205.6 avail Mem
PID USER PR NI VIRT RES SHR S %CPU %MEM TIME+
COMMAND
82399 guest 20 0 65584 5120 4212 R 5.9 0.1 0:00.02 top
1 root 20 0 175932 14212 8924 S 0.0 0.2 0:06.21
systemd
2 root 20 0 0 0 0 S 0.0 0.0 0:00.13
kthreadd
3 root 0 -20 0 0 0 I 0.0 0.0 0:00.00
rcu_gp
4 root 0 -20 0 0 0 I 0.0 0.0 0:00.00
rcu_par_gp
6 root 0 -20 0 0 0 I 0.0 0.0 0:00.00
kworker/0:0H-events_highpri
9 root 0 -20 0 0 0 I 0.0 0.0 0:00.00
mm_percpu_wq
10 root 20 0 0 0 0 S 0.0 0.0 0:02.73
ksoftirqd/0
11 root 20 0 0 0 0 R 0.0 0.0 0:01.10
rcu_sched
12 root rt 0 0 0 0 S 0.0 0.0 0:00.00
migration/0
13 root rt 0 0 0 0 S 0.0 0.0 0:00.04
watchdog/0
14 root 20 0 0 0 0 S 0.0 0.0 0:00.00
cpuhp/0
16 root 20 0 0 0 0 S 0.0 0.0 0:00.00
kdevtmpfs
--More--
```



## 环境变量命令

#### env

显示系统上正在运行的所有环境变量

```bash
$ env | more
SSH_CONNECTION=192.168.86.20 54276 192.168.86.34 22
LANG=en_US.UTF-8
HISTCONTROL=ignoredups
HOSTNAME=localhost.localdomain
which_declare=declare -f
XDG_SESSION_ID=11
USER=reselbob
SELINUX_ROLE_REQUESTED=
PWD=/home/reselbob
SSH_ASKPASS=/usr/libexec/openssh/gnome-ssh-askpass
HOME=/home/reselbob
SSH_CLIENT=192.168.86.20 54276 22
--More--
```



#### export 

创建一个环境变量，并为其复制，然后将该环境变量或值导出到系统

```bash
$ export WEB_PAGE="http://www.redhat.com/en"
```

