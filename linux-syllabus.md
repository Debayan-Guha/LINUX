# LINUX FOR DEVOPS (COMPLETE SYLLABUS)

---

# 1. LINUX FUNDAMENTALS (CORE CONCEPTS)

## 1.1 What is Linux & Why DevOps Uses It
1.1.1 What is Linux operating system  
1.1.2 Linux kernel vs distributions concept  
1.1.3 Why Linux dominates cloud and DevOps  
1.1.4 Server vs desktop Linux differences  
1.1.5 Role of Linux in CI/CD pipelines  
1.1.6 Linux in containers and Kubernetes nodes  

## 1.2 Linux Distributions for DevOps
1.2.1 Ubuntu/Debian family (apt package management)  
1.2.2 RHEL/CentOS/Rocky/Alma family (yum/dnf)  
1.2.3 Alpine Linux (lightweight container base)  
1.2.4 Amazon Linux (AWS cloud environments)  
1.2.5 Choosing the right distro for production  
1.2.6 Distribution-agnostic DevOps skills  

## 1.3 Filesystem Hierarchy Standard (FHS)
1.3.1 `/` (root directory) purpose  
1.3.2 `/bin` vs `/sbin` vs `/usr/bin`  
1.3.3 `/etc` (configuration files)  
1.3.4 `/var` (variable data: logs, spool)  
1.3.5 `/tmp` (temporary files)  
1.3.6 `/home` vs `/root`  
1.3.7 `/proc` and `/sys` (virtual filesystems)  
1.3.8 `/mnt` vs `/media` (mount points)  
1.3.9 `/opt` (optional software)  

---

# 2. ESSENTIAL LINUX COMMANDS (DAY-TO-DAY OPS)

## 2.1 File & Directory Operations
2.1.1 `ls` (list files with options: -l, -a, -h, -R)  
2.1.2 `cd` (change directory, absolute vs relative paths)  
2.1.3 `pwd` (print working directory)  
2.1.4 `mkdir` (create directories, -p for parents)  
2.1.5 `rmdir` vs `rm -rf` (remove directories)  
2.1.6 `touch` (create empty file, update timestamp)  
2.1.7 `cp` (copy files/directories, -r, -p, -a)  
2.1.8 `mv` (move/rename files and directories)  
2.1.9 `rm` (remove files, -i, -f, -r flags)  
2.1.10 `ln` (hard links vs soft/symbolic links)  

## 2.2 File Viewing & Inspection
2.2.1 `cat` (concatenate and display files)  
2.2.2 `less` vs `more` (pagination)  
2.2.3 `head` and `tail` (top/bottom of files)  
2.2.4 `tail -f` (real-time log following)  
2.2.5 `nl` (number lines in files)  
2.2.6 `tac` (reverse order output)  
2.2.7 `wc` (count lines, words, characters)  
2.2.8 `file` (determine file type)  

## 2.3 File Permissions & Ownership
2.3.1 Understanding `rwx` permissions (read, write, execute)  
2.3.2 User (u), Group (g), Others (o) concept  
2.3.3 `chmod` with symbolic (u+x) and octal (755) modes  
2.3.4 `chown` (change file owner and group)  
2.3.5 `chgrp` (change group ownership)  
2.3.6 Special permissions: SUID (4), SGID (2), Sticky Bit (1)  
2.3.7 Understanding `umask` (default permission mask)  
2.3.8 ACLs (Access Control Lists) with `getfacl`/`setfacl`  

## 2.4 Finding Files & Directories
2.4.1 `find` command (search by name, type, size, time)  
2.4.2 `find -exec` (execute commands on found files)  
2.4.3 `locate` vs `find` (database vs real-time search)  
2.4.4 `updatedb` (update locate database)  
2.4.5 `which` (locate executable in PATH)  
2.4.6 `whereis` (find binary, source, man pages)  
2.4.7 `grep -r` (recursive text search in files)  

---

# 3. TEXT PROCESSING & STREAM EDITING (DEVOPS CORE SKILLS)

## 3.1 grep (Global Regular Expression Print)
3.1.1 Basic pattern matching  
3.1.2 `-i` (case-insensitive search)  
3.1.3 `-v` (invert match)  
3.1.4 `-r` / `-R` (recursive directory search)  
3.1.5 `-l` (list matching files only)  
3.1.6 `-n` (show line numbers)  
3.1.7 `-A`/`-B`/`-C` (context lines after/before/around)  
3.1.8 Regular expressions in grep (basic vs extended `-E`)  
3.1.9 `egrep` vs `grep -E` (extended regex)  
3.1.10 Log analysis patterns with grep  

## 3.2 sed (Stream Editor)
3.2.1 `sed` substitution command (`s/old/new/`)  
3.2.2 In-place editing (`-i` flag)  
3.2.3 Address ranges (line numbers, patterns)  
3.2.4 Delete lines (`d` command)  
3.2.5 Print lines (`p` command)  
3.2.6 Append and insert (`a`, `i` commands)  
3.2.7 Multiple sed expressions (`-e` or `;`)  
3.2.8 Using regex groups and backreferences  
3.2.9 Real-world config file manipulation  
3.2.10 Non-interactive file editing for automation  

## 3.3 awk (Pattern Scanning & Processing)
3.3.1 `awk` architecture (pattern {action})  
3.3.2 Field separators (`-F`) and `$1, $2, $NF`  
3.3.3 Built-in variables (NR, NF, FS, OFS, RS)  
3.3.4 Pattern matching in awk  
3.3.5 Arithmetic and string operations  
3.3.6 `if`, `for`, `while` in awk  
3.3.7 `BEGIN` and `END` blocks  
3.3.8 Formatting output with `printf`  
3.3.9 Multi-line record processing  
3.3.10 Log parsing and report generation  

## 3.4 cut, sort, uniq, tr
3.4.1 `cut` (extract columns: `-f`, `-d`, `-c`)  
3.4.2 `sort` (sorting lines: `-n`, `-r`, `-k`, `-t`)  
3.4.3 `uniq` (report/omit repeated lines, requires sorted input)  
3.4.4 `tr` (translate or delete characters)  
3.4.5 Pipeline combinations (`cut|sort|uniq` pattern)  
3.4.6 Real-world data extraction examples  

## 3.5 diff, comm, patch
3.5.1 `diff` (compare files line by line)  
3.5.2 `diff -u` (unified diff format)  
3.5.3 `comm` (compare sorted files)  
3.5.4 `patch` (apply diff patches)  
3.5.5 Use cases in configuration drift detection  

## 3.6 Regular Expressions Deep Dive
3.6.1 Basic regex vs Extended regex (BRE vs ERE)  
3.6.2 Character classes (`[a-z]`, `[^0-9]`)  
3.6.3 Quantifiers (`*`, `+`, `?`, `{n,m}`)  
3.6.4 Anchors (`^` start, `$` end, `\<` word boundary)  
3.6.5 Grouping `()` and alternation `|`  
3.6.6 Escape sequences (`\.`, `\*`, `\\`)  
3.6.7 Greedy vs lazy matching  
3.6.8 Practical regex for log parsing and validation  

---

# 4. PROCESS MANAGEMENT

## 4.1 Viewing Processes
4.1.1 `ps aux` vs `ps -ef` (process snapshot)  
4.1.2 `ps` columns explained (PID, PPID, CPU, MEM, STAT)  
4.1.3 Process states (R, S, D, Z, T)  
4.1.4 `top` (real-time process monitoring)  
4.1.5 `htop` (improved interactive viewer)  
4.1.6 `pgrep` and `pidof` (find processes by name)  

## 4.2 Managing Processes
4.2.1 Foreground vs background processes (`&`)  
4.2.2 `jobs`, `fg`, `bg` (job control)  
4.2.3 `kill` (send signals to processes)  
4.2.4 Signal types (SIGTERM 15, SIGKILL 9, SIGHUP 1)  
4.2.5 `killall` and `pkill` (kill by name)  
4.2.6 `nice` and `renice` (process priority)  
4.2.7 Zombie processes and orphaned processes  

## 4.3 Process Monitoring & Troubleshooting
4.3.1 `strace` (trace system calls)  
4.3.2 `lsof` (list open files and network connections)  
4.3.3 `/proc` filesystem exploration  
4.3.4 `ulimit` (user process/resource limits)  
4.3.5 `nohup` and `disown` (detach processes from terminal)  
4.3.6 `wait` command for process synchronization  

---

# 5. MEMORY & DISK MANAGEMENT

## 5.1 Memory Monitoring
5.1.1 `free -h` (memory usage overview)  
5.1.2 Understanding buffers vs cache  
5.1.3 `vmstat` (virtual memory statistics)  
5.1.4 `top`/`htop` memory columns  
5.1.5 `/proc/meminfo` detailed analysis  
5.1.6 Swap space usage and tuning  
5.1.7 OOM (Out-Of-Memory) killer behavior  

## 5.2 Disk Usage & Analysis
5.2.1 `df -h` (filesystem disk usage)  
5.2.2 `du -sh` (directory size calculation)  
5.2.3 `du -sh * | sort -h` (find largest directories)  
5.2.4 `ncdu` (interactive disk usage analyzer)  
5.2.5 Inode exhaustion troubleshooting  
5.2.6 Disk partitioning (`fdisk`, `lsblk`, `parted`)  
5.2.7 Filesystem types (ext4, XFS, btrfs)  
5.2.8 Mounting and unmounting (`mount`, `umount`, `/etc/fstab`)  

## 5.3 Logical Volume Manager (LVM)
5.3.1 PV (Physical Volume), VG (Volume Group), LV (Logical Volume)  
5.3.2 `pvcreate`, `vgcreate`, `lvcreate`  
5.3.3 Extending LVs without downtime  
5.3.4 Reducing LVs (risks and precautions)  
5.3.5 LVM snapshots for backups  
5.3.6 LVM in cloud and virtualized environments  

---

# 6. USER & GROUP ADMINISTRATION

## 6.1 User Management
6.1.1 `/etc/passwd`, `/etc/shadow`, `/etc/group` files  
6.1.2 `useradd` vs `adduser` (creating users)  
6.1.3 `passwd` (setting/changing passwords)  
6.1.4 `usermod` (modifying user properties)  
6.1.5 `userdel` (deleting users)  
6.1.6 `/etc/skel` (skeleton directory for new users)  
6.1.7 `who`, `w`, `last`, `lastlog` (user session tracking)  

## 6.2 Group Management
6.2.1 `groupadd`, `groupmod`, `groupdel`  
6.2.2 Primary vs secondary groups  
6.2.3 Adding users to groups (`usermod -aG`)  
6.2.4 `groups` command (show group membership)  
6.2.5 `id` command (UID, GID, group info)  

## 6.3 Sudo (Superuser Do)
6.3.1 What is sudo and why it's used  
6.3.2 `/etc/sudoers` file syntax  
6.3.3 `visudo` (safe sudoers editing)  
6.3.4 Granting specific command access  
6.3.5 Passwordless sudo configuration (`NOPASSWD`)  
6.3.6 Sudo vs su (switch user) differences  
6.3.7 Sudo logging and auditing  

---

# 7. NETWORKING FUNDAMENTALS

## 7.1 Network Configuration
7.1.1 `ip` command (modern replacement for ifconfig)  
7.1.2 `ip addr`, `ip link`, `ip route`  
7.1.3 Legacy `ifconfig`, `route`, `netstat`  
7.1.4 `/etc/network/interfaces` (Debian) vs `/etc/sysconfig/network-scripts/` (RHEL)  
7.1.5 NetworkManager vs systemd-networkd  
7.1.6 DHCP client configuration  

## 7.2 Network Inspection & Debugging
7.2.1 `ping` (ICMP connectivity test)  
7.2.2 `traceroute` vs `tracepath` (path discovery)  
7.2.3 `mtr` (combined ping + traceroute)  
7.2.4 `nslookup` and `dig` (DNS resolution)  
7.2.5 `host` command (DNS lookup)  
7.2.6 `/etc/resolv.conf` (DNS nameserver configuration)  
7.2.7 `/etc/hosts` (static hostname mapping)  

## 7.3 Port & Connection Analysis
7.3.1 `ss` (socket statistics, modern netstat replacement)  
7.3.2 `netstat` (legacy connection viewing)  
7.3.3 `lsof -i` (list open network ports)  
7.3.4 `nmap` (port scanning basics for debugging)  
7.3.5 `telnet` and `nc` (netcat) for port testing  

## 7.4 Firewall Management
7.4.1 `ufw` (Uncomplicated Firewall for Ubuntu/Debian)  
7.4.2 `firewalld` (RHEL/CentOS/Fedora)  
7.4.3 `iptables` fundamentals (chains: INPUT, OUTPUT, FORWARD)  
7.4.4 Allowing/denying specific ports and IPs  
7.4.5 Saving and restoring firewall rules  

---

# 8. PACKAGE MANAGEMENT

## 8.1 APT (Debian/Ubuntu Family)
8.1.1 `apt update` vs `apt upgrade` vs `apt full-upgrade`  
8.1.2 `apt install`, `apt remove`, `apt purge`  
8.1.3 `apt search`, `apt show` (package discovery)  
8.1.4 `apt list --upgradable`  
8.1.5 `/etc/apt/sources.list` and repository management  
8.1.6 `dpkg` (low-level package tool)  
8.1.7 Fixing broken dependencies (`apt --fix-broken install`)  

## 8.2 YUM/DNF (RHEL/CentOS/Rocky Family)
8.2.1 `yum` vs `dnf` differences  
8.2.2 `dnf install`, `dnf remove`, `dnf update`  
8.2.3 `dnf search`, `dnf info`  
8.2.4 `dnf repolist` (repository management)  
8.2.5 `rpm` (low-level package tool)  
8.2.6 `dnf history` (transaction rollback)  
8.2.7 EPEL (Extra Packages for Enterprise Linux)  

## 8.3 Managing Repositories & GPG Keys
8.3.1 Adding third-party repositories (PPAs on Ubuntu, .repo on RHEL)  
8.3.2 GPG key import and verification  
8.3.3 Repository priority and pinning  
8.3.4 Creating a local repository mirror  

---

# 9. SERVICES & SYSTEMD

## 9.1 systemd Fundamentals
9.1.1 What is systemd (init system)  
9.1.2 Units: `.service`, `.timer`, `.socket`, `.target`  
9.1.3 `systemctl` command structure  
9.1.4 `systemctl start`, `stop`, `restart`, `reload`  
9.1.5 `systemctl enable`, `disable` (boot-time activation)  
9.1.6 `systemctl status` (service health and logs)  
9.1.7 `systemctl is-active`, `is-enabled`, `is-failed`  

## 9.2 Service Management
9.2.1 Viewing all active services (`systemctl list-units`)  
9.2.2 Viewing failed services (`systemctl --failed`)  
9.2.3 Creating custom systemd service files  
9.2.4 Service dependencies (`After=`, `Requires=`, `Wants=`)  
9.2.5 Restart policies (`Restart=always`, `on-failure`, `no`)  
9.2.6 Environment variable injection in services  
9.2.7 Service hardening (PrivateTmp, NoNewPrivileges)  

## 9.3 systemd Journal (Logging)
9.3.1 `journalctl` basics  
9.3.2 Viewing logs for a specific service (`journalctl -u nginx`)  
9.3.3 `journalctl -f` (follow real-time logs)  
9.3.4 `journalctl --since` and `--until` (time-based filtering)  
9.3.5 Persistent vs volatile journal storage  
9.3.6 Journal size limits and rotation  

## 9.4 systemd Timers (Cron Replacement)
9.4.1 What are systemd timers  
9.4.2 Creating a timer unit  
9.4.3 `OnCalendar`, `OnBootSec`, `OnUnitActiveSec` directives  
9.4.4 systemd timers vs cron comparisons  
9.4.5 `systemctl list-timers`  

---

# 10. CRON & TASK SCHEDULING

## 10.1 Cron Fundamentals
10.1.1 What is cron (time-based job scheduler)  
10.1.2 Crontab syntax (minute, hour, day, month, weekday)  
10.1.3 `crontab -e`, `-l`, `-r` commands  
10.1.4 User-specific crontabs vs system crontab (`/etc/crontab`)  
10.1.5 Cron environment variables (PATH, SHELL, MAILTO)  

## 10.2 Advanced Cron Patterns
10.2.1 Special strings (`@reboot`, `@daily`, `@hourly`, `@weekly`, `@monthly`, `@yearly`)  
10.2.2 Step values (`*/5 * * * *` for every 5 minutes)  
10.2.3 Multiple values using commas (`1,15,30 * * * *`)  
10.2.4 Ranges (`1-10 * * * *`)  
10.2.5 Redirecting cron output (stdout, stderr, logging)  

## 10.3 Cron Troubleshooting & Best Practices
10.3.1 Checking cron logs (`/var/log/syslog`, `/var/log/cron`)  
10.3.2 Common cron failures (PATH issues, environment missing)  
10.3.3 Using wrapper scripts for complex cron jobs  
10.3.4 Lock files to prevent overlapping runs  
10.3.5 Anacron for systems not running 24/7  

---

# 11. SHELL SCRIPTING (BASH FOR DEVOPS)

## 11.1 Script Basics
11.1.1 Shebang (`#!/bin/bash`)  
11.1.2 Making scripts executable (`chmod +x`)  
11.1.3 Variables (system vs user-defined, `$VAR`, `${VAR}`)  
11.1.4 Command substitution (`$(command)` vs backticks)  
11.1.5 Arithmetic operations (`$((...))`)  
11.1.6 Positional parameters (`$1`, `$2`, `$@`, `$#`, `$?`)  
11.1.7 Reading user input (`read` command)  

## 11.2 Conditional Statements
11.2.1 `if-then-else` syntax  
11.2.2 `elif` (else if)  
11.2.3 `case` statements (pattern matching)  
11.2.4 Test operators (`[ ]` vs `[[ ]]`)  
11.2.5 String comparisons (`=`, `!=`, `-z`, `-n`)  
11.2.6 Numeric comparisons (`-eq`, `-ne`, `-lt`, `-le`, `-gt`, `-ge`)  
11.2.7 File tests (`-f`, `-d`, `-e`, `-x`, `-r`, `-w`, `-s`)  
11.2.8 Logical operators (`&&`, `||`, `!`)  

## 11.3 Loops & Iteration
11.3.1 `for` loop (over list, range, files)  
11.3.2 `while` loop (condition-based)  
11.3.3 `until` loop (opposite of while)  
11.3.4 `break` and `continue` statements  
11.3.5 Loop control patterns in DevOps scripts  

## 11.4 Functions
11.4.1 Defining and calling functions  
11.4.2 Function arguments (`$1`, `$2` inside function)  
11.4.3 Return values (exit codes, `return` keyword)  
11.4.4 Local variables (`local var`)  
11.4.5 Function libraries and sourcing scripts  

## 11.5 Arrays & Data Structures
11.5.1 Indexed arrays (`array=(a b c)`)  
11.5.2 Associative arrays (Bash 4+, `declare -A`)  
11.5.3 Array operations (append, slicing, length)  
11.5.4 Iterating over array elements  

## 11.6 Exit Codes & Error Handling
11.6.1 Understanding exit codes (0 = success, non-zero = failure)  
11.6.2 `$?` variable (last command exit code)  
11.6.3 `set -e` (exit on error)  
11.6.4 `set -u` (treat unset variables as error)  
11.6.5 `set -x` (debug mode)  
11.6.6 `set -o pipefail` (detect failures in pipelines)  
11.6.7 Trap signals (`trap` for cleanup)  

## 11.7 Real-World DevOps Scripting Patterns
11.7.1 Logging functions with timestamps  
11.7.2 Configuration file parsing  
11.7.3 Health check scripts for containers  
11.7.4 Backup automation scripts  
11.7.5 Deployment and rollback scripts  
11.7.6 Monitoring and alerting scripts  
11.7.7 Idempotent script design  

---

# 12. SSH (SECURE SHELL)

## 12.1 SSH Fundamentals
12.1.1 What is SSH and why it's used  
12.1.2 `ssh` command syntax  
12.1.3 Password-based authentication  
12.1.4 SSH daemon (`sshd`) configuration (`/etc/ssh/sshd_config`)  

## 12.2 Key-Based Authentication
12.2.1 Generating key pairs (`ssh-keygen -t rsa -b 4096`)  
12.2.2 Ed25519 vs RSA key types  
12.2.3 `~/.ssh/id_rsa` (private key) and `~/.ssh/id_rsa.pub` (public key)  
12.2.4 Copying public key (`ssh-copy-id`)  
12.2.5 `~/.ssh/authorized_keys` file  
12.2.6 Passphrase vs passwordless keys  
12.2.7 `ssh-agent` and `ssh-add` (key management)  

## 12.3 SSH Configuration
12.3.1 `~/.ssh/config` (per-user client configuration)  
12.3.2 Host aliases, User, Port, IdentityFile directives  
12.3.3 ProxyJump and ProxyCommand (bastion hosts)  
12.3.4 SSH multiplexing (ControlMaster, ControlPath)  
12.3.5 Server-side hardening (disable root login, password auth)  
12.3.6 Changing default SSH port  

## 12.4 Secure File Transfer
12.4.1 `scp` (secure copy) syntax and recursion (`-r`)  
12.4.2 `rsync` (incremental file transfer)  
12.4.3 `rsync -avz` (archive, verbose, compress)  
12.4.4 `rsync --delete` (source/destination sync)  
12.4.5 `sftp` (interactive FTP over SSH)  

## 12.5 SSH Tunneling & Port Forwarding
12.5.1 Local port forwarding (`-L`)  
12.5.2 Remote port forwarding (`-R`)  
12.5.3 Dynamic port forwarding (SOCKS proxy `-D`)  
12.5.4 Use cases in secure database access  
12.5.5 SSH tunneling for Kubernetes API access  

---

# 13. ARCHIVING & COMPRESSION

## 13.1 tar (Tape Archive)
13.1.1 `tar cvf` (create archive)  
13.1.2 `tar xvf` (extract archive)  
13.1.3 `tar tvf` (list contents)  
13.1.4 `-z` (gzip compression), `-j` (bzip2), `-J` (xz)  
13.1.5 `--exclude` patterns  
13.1.6 `-C` (change directory before extraction)  

## 13.2 Compression Tools
13.2.1 `gzip` and `gunzip`  
13.2.2 `bzip2` and `bunzip2` (better compression, slower)  
13.2.3 `xz` and `unxz` (high compression ratio)  
13.2.4 `zip` and `unzip` (cross-platform compatibility)  
13.2.5 Compression level tuning (`-1` to `-9`)  

## 13.3 Real-World Backup Patterns
13.3.1 Backing up directories with timestamped archives  
13.3.2 Incremental backups using tar  
13.3.3 Encrypting archives with `gpg`  
13.3.4 Automating backup rotation scripts  

---

# 14. ENVIRONMENT VARIABLES & PATH

## 14.1 Environment vs Shell Variables
14.1.1 Difference between environment and shell variables  
14.1.2 `export` (making variables available to child processes)  
14.1.3 `env` and `printenv` commands  
14.1.4 `set` (display all variables)  
14.1.5 `unset` (remove variables)  

## 14.2 Important Environment Variables
14.2.1 `PATH` (executable search path)  
14.2.2 `HOME`, `USER`, `SHELL`, `TERM`  
14.2.3 `LANG` and `LC_ALL` (locale settings)  
14.2.4 `PS1` (prompt customization)  
14.2.5 `http_proxy`, `https_proxy`, `no_proxy`  

## 14.3 Shell Configuration Files
14.3.1 `/etc/profile` (system-wide)  
14.3.2 `~/.bashrc` (interactive non-login shell)  
14.3.3 `~/.bash_profile` / `~/.profile` (login shell)  
14.3.4 `~/.bash_logout` (logout actions)  
14.3.5 Order of execution and precedence  
14.3.6 Aliases and functions in `.bashrc`  

---

# 15. LINUX FOR CONTAINERS (DOCKER & KUBERNETES CONTEXT)

## 15.1 Linux Features Enabling Containers
15.1.1 Namespaces (PID, NET, MNT, UTS, IPC, USER, CGROUP)  
15.1.2 Cgroups (resource limits: CPU, memory, disk I/O)  
15.1.3 Union filesystems (OverlayFS, AUFS)  
15.1.4 Chroot vs pivot_root  

## 15.2 Container Runtime Interaction
15.2.1 Docker daemon communication (Unix socket `/var/run/docker.sock`)  
15.2.2 Container logs on host (`/var/lib/docker/containers/`)  
15.2.3 Inspecting container processes from host (`docker top`)  
15.2.4 Running commands inside containers (`docker exec`, `kubectl exec`)  

## 15.3 Linux Debugging in Container Context
15.3.1 Using `nsenter` to enter container namespaces  
15.3.2 Debugging Kubernetes nodes with privileged containers  
15.3.3 `crictl` for containerd/CRI-O debugging  
15.3.4 Container runtime socket paths  

---

# 16. PERFORMANCE MONITORING & TROUBLESHOOTING

## 16.1 System Performance Tools
16.1.1 `uptime` (load averages)  
16.1.2 `dmesg` (kernel ring buffer)  
16.1.3 `iostat` (CPU and disk I/O statistics)  
16.1.4 `mpstat` (per-processor statistics)  
16.1.5 `sar` (system activity reporter for historical data)  

## 16.2 Network Performance
16.2.1 `iperf3` (bandwidth testing)  
16.2.2 `iftop` (real-time bandwidth per connection)  
16.2.3 `nethogs` (bandwidth per process)  
16.2.4 `tcpdump` (packet capture and analysis)  
16.2.5 `wireshark` and `tshark` (deep packet inspection)  

## 16.3 Common Performance Issues
16.3.1 High CPU usage troubleshooting  
16.3.2 Memory leaks and OOM issues  
16.3.3 Disk I/O bottlenecks  
16.3.4 Network latency and packet loss  
16.3.5 File descriptor exhaustion (`ulimit -n`)  
16.3.6 Zombie process accumulation  

---

# 17. LINUX SECURITY HARDENING (FOR DEVOPS)

## 17.1 System Hardening Basics
17.1.1 Principle of least privilege  
17.1.2 Disabling unnecessary services  
17.1.3 Regular security updates (`unattended-upgrades`)  
17.1.4 Fail2ban for brute force protection  

## 17.2 File Integrity & Auditing
17.2.1 `auditd` (Linux Auditing System)  
17.2.2 `aide` (Advanced Intrusion Detection Environment)  
17.2.3 Monitoring critical files (`/etc/passwd`, `/etc/shadow`, `/etc/sudoers`)  

## 17.3 SELinux & AppArmor
17.3.1 What is SELinux (Security-Enhanced Linux)  
17.3.2 SELinux modes (Enforcing, Permissive, Disabled)  
17.3.3 SELinux contexts and booleans  
17.3.4 What is AppArmor (path-based MAC)  
17.3.5 AppArmor profiles for containers  
17.3.6 SELinux vs AppArmor comparison  

---

# 18. LOG MANAGEMENT & ANALYSIS

## 18.1 System Logs Locations
18.1.1 `/var/log/syslog` (general system log)  
18.1.2 `/var/log/auth.log` (authentication events)  
18.1.3 `/var/log/kern.log` (kernel messages)  
18.1.4 `/var/log/dpkg.log` / `/var/log/yum.log` (package management)  
18.1.5 Application logs under `/var/log/`  

## 18.2 Log Rotation
18.2.1 `logrotate` configuration (`/etc/logrotate.conf`)  
18.2.2 Per-application logrotate rules (`/etc/logrotate.d/`)  
18.2.3 Size vs time-based rotation  
18.2.4 Compression, delay compression, and post-rotate scripts  

## 18.3 Centralized Logging for DevOps
18.3.1 Forwarding logs to ELK/Loki stack  
18.3.2 `rsyslog` configuration for remote logging  
18.3.3 `journalctl` remote forwarding  

---

# 19. LINUX FOR CLOUD & INFRASTRUCTURE AS CODE

## 19.1 Cloud-Init & User Data
19.1.1 What is cloud-init for VM provisioning  
19.1.2 Writing cloud-init user-data scripts  
19.1.3 Installing packages, creating users, running commands at boot  

## 19.2 Configuration Management (Agent vs Agentless)
19.2.1 Ansible fundamentals (SSH-based, agentless)  
19.2.2 Writing Ansible playbooks for Linux configuration  
19.2.3 Puppet/Chef agent-based model overview  

## 19.3 Linux in CI/CD Pipelines
19.3.1 Writing pipeline scripts that run on Linux runners  
19.3.2 Common Linux commands in GitHub Actions, GitLab CI, Jenkins  
19.3.3 Caching dependencies on Linux CI runners  

---

# 20. COMMON TROUBLESHOOTING SCENARIOS (INTERVIEW FOCUS)

## 20.1 "High CPU usage on a Linux server"
20.1.1 Using `top`/`htop` to identify offending processes  
20.1.2 `strace -p PID` for syscall analysis  
20.1.3 Checking for fork bombs and runaway loops  

## 20.2 "Disk full error but `df` shows space available"
20.2.1 Inode exhaustion check (`df -i`)  
20.2.2 Deleted files held open by processes (`lsof | grep deleted`)  
20.2.3 Filesystem reserved blocks (`tune2fs`)  

## 20.3 "Port already in use but no process listening"
20.3.1 `ss -tlnp` to find listening processes  
20.3.2 TIME_WAIT connections and port reuse  
20.3.3 `netstat -tunap` alternative  

## 20.4 "Cannot SSH to server"
20.4.1 Network connectivity check (`ping`, `telnet <port> 22`)  
20.4.2 SSH daemon status (`systemctl status sshd`)  
20.4.3 Firewall rules checking (`iptables -L`, `ufw status`)  
20.4.4 `~/.ssh/authorized_keys` permissions (must be 600)  
20.4.5 `/etc/ssh/sshd_config` misconfiguration  

## 20.5 "Command not found for newly installed package"
20.5.1 `echo $PATH` verification  
20.5.2 Package installation verification (`dpkg -l | grep <pkg>`)  
20.5.3 Running `hash -r` to clear command cache  

---

# 21. HANDS-ON LABS (DO THESE ON YOUR TERMINAL)

## 21.1 Filesystem & File Operations Labs

### 21.1.1 Create and Navigate Directory Structure
21.1.1.1 Create the following directory tree under `/tmp/devops-lab/`:
- `project/`
  - `src/`
  - `logs/`
  - `backup/`
  - `config/`
21.1.1.2 Navigate into `project/src/` using absolute path
21.1.1.3 Navigate back to `project/` using relative path
21.1.1.4 Print current working directory at each step
21.1.1.5 Create empty files: `app.py`, `Dockerfile`, `nginx.conf` inside `config/`
21.1.1.6 Copy `nginx.conf` to `backup/nginx.conf.bak`
21.1.1.7 Move `app.py` to `src/app.py`
21.1.1.8 Create a symbolic link `config/nginx-link.conf` pointing to `config/nginx.conf`
21.1.1.9 Delete the `logs/` directory (which is empty at this point)
21.1.1.10 Verify the final directory structure using `tree` or `find`

### 21.1.2 File Permissions Lab
21.1.2.1 Create a file `secret.sh` with content `#!/bin/bash\necho "Hello"`
21.1.2.2 Set permission so only owner can read, write, and execute (700)
21.1.2.3 Create another file `team.sh` with same content
21.1.2.4 Change group ownership to a group that exists on your system
21.1.2.5 Set permission so group can read and execute (750)
21.1.2.6 Create a directory `shared/` with sticky bit (1777)
21.1.2.7 Create a file `suid-binary` and set SUID bit (4755)
21.1.2.8 Verify all permissions using `ls -l`
21.1.2.9 Try to execute `secret.sh` as a different user (observe permission denied)
21.1.2.10 Remove all created files and directories

### 21.1.3 Find Files Lab
21.1.3.1 Create 10 files with `.log` extension in `/tmp/find-lab/` with names `app1.log` to `app10.log`
21.1.3.2 Set different modification dates using `touch -t`
21.1.3.3 Find all `.log` files modified in the last 1 hour
21.1.3.4 Find all `.log` files larger than 1KB
21.1.3.5 Find and delete all `.tmp` files in one command
21.1.3.6 Find all empty directories under `/tmp/`
21.1.3.7 Use `find -exec` to rename all `.log` files to `.old`
21.1.3.8 Use `locate` to find `nginx.conf` (update database first)
21.1.3.9 Use `which` and `whereis` for `python3` and `systemctl`
21.1.3.10 Clean up `/tmp/find-lab/`

---

## 21.2 Text Processing Labs

### 21.2.1 grep Lab
21.2.1.1 Create a log file `sample.log` with mixed content containing INFO, WARN, ERROR levels
21.2.1.2 Extract all lines containing "ERROR" (case-sensitive)
21.2.1.3 Extract all lines containing "error" (case-insensitive)
21.2.1.4 Extract all lines NOT containing "INFO"
21.2.1.5 Extract all lines containing "ERROR" and show line numbers
21.2.1.6 Extract all lines containing "ERROR" and show 2 lines before and 1 line after
21.2.1.7 Count how many lines contain "WARN"
21.2.1.8 Extract all IP addresses from the log file using regex
21.2.1.9 Extract all email addresses from a dummy text file
21.2.1.10 Recursively search for the word "TODO" in all `.py` files under a directory

### 21.2.2 sed Lab
21.2.2.1 Create `config.txt` with `port=8080` and change it to `port=9090` using sed (dry run first)
21.2.2.2 Edit `config.txt` in-place to change the port
21.2.2.3 Delete all empty lines from a file
21.2.2.4 Delete all lines starting with `#` (comments) from a file
21.2.2.5 Append a line "Log rotation completed" after every line containing "ERROR"
21.2.2.6 Change date format from `YYYY-MM-DD` to `DD/MM/YYYY` in a file
21.2.2.7 Remove trailing whitespace from all lines
21.2.2.8 Replace all occurrences of `localhost` with `127.0.0.1` in a file
21.2.2.9 Extract only lines 50-100 from a large log file
21.2.2.10 Combine multiple sed commands using `-e` or `;`

### 21.2.3 awk Lab
21.2.3.1 Create `employee.csv` with columns: name, department, salary
21.2.3.2 Print only the first column (names)
21.2.3.3 Print name and salary columns
21.2.3.4 Print lines where salary > 50000
21.2.3.5 Calculate total salary of all employees
21.2.3.6 Calculate average salary of all employees
21.2.3.7 Print department name and total salary per department
21.2.3.8 Find the highest salary and print employee name
21.2.3.9 Count number of employees per department
21.2.3.10 Format output as table using `printf`

### 21.2.4 Pipeline Lab (cut, sort, uniq, tr)
21.2.4.1 Create `access.log` with dummy Apache log entries
21.2.4.2 Extract unique IP addresses from the log
21.2.4.3 Find top 5 IPs with highest request count
21.2.4.4 Count occurrences of each HTTP status code (200, 404, 500)
21.2.4.5 Extract all URLs accessed more than 10 times
21.2.4.6 Convert all log entries to uppercase and save to new file
21.2.4.7 Remove duplicate lines from a sorted file
21.2.4.8 Sort a file by the second column (numerically)
21.2.4.9 Find common lines between two files using `comm`
21.2.4.10 Find lines unique to file A and file B separately

---

## 21.3 Process Management Labs

### 21.3.1 Viewing and Monitoring Processes
21.3.1.1 Run `sleep 300` in the background
21.3.1.2 Use `ps aux` to find the PID of that `sleep` process
21.3.1.3 Use `pgrep` to find the same PID
21.3.1.4 Run `top` and sort by memory usage (press `M` key)
21.3.1.5 Run `htop` (install if missing) and kill a process from the UI
21.3.1.6 Use `ps auxf` to view process tree
21.3.1.7 Identify the parent PID (PPID) of your shell
21.3.1.8 List all processes owned by `root`
21.3.1.9 Use `ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%cpu` to see CPU hogs
21.3.1.10 Observe process state (R, S, D, Z) using `ps`

### 21.3.2 Controlling Processes
21.3.2.1 Start a long-running command (e.g., `ping google.com`) and suspend it using `Ctrl+Z`
21.3.2.2 View background jobs using `jobs`
21.3.2.3 Resume the job in the background using `bg`
21.3.2.4 Bring the job back to foreground using `fg`
21.3.2.5 Start a process with `&` to run in background directly
21.3.2.6 Kill a process using its PID with SIGTERM
21.3.2.7 Kill a process using SIGKILL and observe the difference
21.3.2.8 Use `killall` to kill all `ping` processes
21.3.2.9 Use `pkill -f "ping google.com"` to kill by command pattern
21.3.2.10 Start a process with lower priority using `nice`

### 21.3.3 Process Debugging Lab
21.3.3.1 Write a simple Python script that runs an infinite loop
21.3.3.2 Run it and use `strace -p <PID>` to see system calls
21.3.3.3 Use `lsof -p <PID>` to see all open files and network connections
21.3.3.4 Explore `/proc/<PID>/` directory (cat `status`, `cmdline`, `environ`)
21.3.3.5 Set `ulimit -n 100` and test file descriptor limit
21.3.3.6 Create a process that runs after terminal closes using `nohup`
21.3.3.7 Detach a running process using `disown`
21.3.3.8 Create a zombie process (fork child that exits but parent doesn't wait)
21.3.3.9 Verify zombie state using `ps aux | grep Z`
21.3.3.10 Clean up zombie process by killing parent

---

## 21.4 Memory & Disk Management Labs

### 21.4.1 Memory Monitoring Lab
21.4.1.1 Run `free -h` and identify total, used, available memory
21.4.1.2 Run `vmstat 2 5` and understand each column (r, b, si, so, us, sy, id)
21.4.1.3 Use `top` to sort by memory usage (press `M`)
21.4.1.4 Check swap usage: `swapon --show`
21.4.1.5 Create a 256MB swap file and enable it (then disable and remove)
21.4.1.6 View detailed memory info: `cat /proc/meminfo`
21.4.1.7 Check for OOM killer events: `dmesg | grep -i "oom" | tail -10`
21.4.1.8 Run `stress --vm 1 --vm-bytes 512M` to simulate memory pressure
21.4.1.9 While stress runs, monitor with `free` and `vmstat`
21.4.1.10 Clear page cache: `sync && echo 3 | sudo tee /proc/sys/vm/drop_caches`

### 21.4.2 Disk Usage Lab
21.4.2.1 Run `df -h` and identify filesystems with high usage
21.4.2.2 Run `df -i` to check inode usage
21.4.2.3 Create 100,000 small files in a directory and check inode usage
21.4.2.4 Find the largest directory under `/var` using `du -sh /var/* | sort -h`
21.4.2.5 Run `ncdu` (install if needed) and navigate through the filesystem
21.4.2.6 Identify which files are consuming most space in `/tmp`
21.4.2.7 List block devices: `lsblk`
21.4.2.8 Mount a new temporary filesystem: `sudo mount -t tmpfs tmpfs /mnt/tmp`
21.4.2.9 Check `/etc/fstab` to understand persistent mounts
21.4.2.10 Unmount the temporary filesystem

### 21.4.3 LVM Lab (Requires spare disk or VM)
21.4.3.1 List physical volumes: `sudo pvs`
21.4.3.2 Create a physical volume on `/dev/sdb` (if available)
21.4.3.3 Create a volume group named `vg_data`
21.4.3.4 Create a logical volume named `lv_data` of size 1GB
21.4.3.5 Format it with ext4: `sudo mkfs.ext4 /dev/vg_data/lv_data`
21.4.3.6 Mount it to `/mnt/data`
21.4.3.7 Extend the logical volume by 500MB
21.4.3.8 Resize the filesystem: `sudo resize2fs /dev/vg_data/lv_data`
21.4.3.9 Create an LVM snapshot for backup testing
21.4.3.10 Remove the volume group, physical volume, and logical volume

---

## 21.5 User & Group Administration Labs

### 21.5.1 User Management Lab
21.5.1.1 Create a user `devops_user` with home directory `/home/devops_user`
21.5.1.2 Set password for `devops_user`
21.5.1.3 Create a user `app_user` with no login shell (`/usr/sbin/nologin`)
21.5.1.4 Create a system user `kube` (UID < 1000)
21.5.1.5 Modify `devops_user` to have expiry date 30 days from now
21.5.1.6 Lock the `app_user` account using `usermod -L`
21.5.1.7 Verify locked status in `/etc/shadow`
21.5.1.8 Delete `app_user` but keep home directory
21.5.1.9 Check login history: `last` and `lastlog`
21.5.1.10 See currently logged in users: `who`, `w`

### 21.5.2 Group Management Lab
21.5.2.1 Create a group `docker`
21.5.2.2 Create a group `k8s`
21.5.2.3 Add `devops_user` to both groups (secondary)
21.5.2.4 Verify group membership: `id devops_user` and `groups devops_user`
21.5.2.5 Change primary group of `devops_user` to `docker`
21.5.2.6 Remove `devops_user` from `k8s` group
21.5.2.7 Delete the `k8s` group
21.5.2.8 Create a shared directory `/opt/shared` with SGID so all files inherit group
21.5.2.9 Verify SGID works by creating a file in the directory
21.5.2.10 List all groups on system: `cut -d: -f1 /etc/group`

### 21.5.3 Sudo Lab
21.5.3.1 Grant `devops_user` permission to run `systemctl` as root
21.5.3.2 Grant `devops_user` permission to run `apt update` and `apt upgrade` only
21.5.3.3 Configure passwordless sudo for `devops_user` for specific commands
21.5.3.4 Test sudo access with `sudo -l`
21.5.3.5 View sudo logs in `/var/log/auth.log`
21.5.3.6 Create a sudo rule allowing a group `admins` full sudo access
21.5.3.7 Set sudo timeout to 15 minutes
21.5.3.8 Prevent sudo from asking for password for certain commands
21.5.3.9 Use `visudo` to validate syntax before saving
21.5.3.10 Switch to a user: `sudo -u devops_user bash`

---

## 21.6 Networking Labs

### 21.6.1 Network Configuration Lab
21.6.1.1 View all network interfaces: `ip link show`
21.6.1.2 View IP addresses: `ip addr show`
21.6.1.3 View routing table: `ip route show`
21.6.1.4 Add a temporary IP address: `sudo ip addr add 192.168.100.10/24 dev eth0`
21.6.1.5 Remove the temporary IP address
21.6.1.6 Check ARP table: `ip neigh show`
21.6.1.7 View DNS configuration: `cat /etc/resolv.conf`
21.6.1.8 Add a test entry to `/etc/hosts` for `test.local`
21.6.1.9 Ping `test.local` to verify resolution
21.6.1.10 Restart networking service: `sudo systemctl restart networking` (or NetworkManager)

### 21.6.2 Network Debugging Lab
21.6.2.1 Ping `google.com` and check packet loss
21.6.2.2 Use `traceroute google.com` to see network path
21.6.2.3 Use `mtr google.com` (combined ping + traceroute)
21.6.2.4 Use `dig google.com` to see DNS resolution details
21.6.2.5 Use `nslookup kubernetes.io` for DNS query
21.6.2.6 Use `host -t A amazon.com`
21.6.2.7 Use `ss -tlnp` to see listening TCP ports and associated processes
21.6.2.8 Use `ss -tup` to see active connections with process names
21.6.2.9 Use `lsof -i :80` to see what is using port 80
21.6.2.10 Use `nc -zv google.com 443` to test port connectivity

### 21.6.3 Firewall Lab
21.6.3.1 Install `ufw` if not present: `sudo apt install ufw`
21.6.3.2 Enable UFW and check status: `sudo ufw status`
21.6.3.3 Allow SSH traffic (port 22): `sudo ufw allow 22`
21.6.3.4 Allow HTTP (80) and HTTPS (443) traffic
21.6.3.5 Deny all incoming traffic except allowed ports
21.6.3.6 Check UFW rules: `sudo ufw status numbered`
21.6.3.7 Delete a rule by number
21.6.3.8 Disable UFW: `sudo ufw disable`
21.6.3.9 (Alternative) Use `iptables` to block ICMP: `sudo iptables -A INPUT -p icmp -j DROP`
21.6.3.10 Flush iptables rules: `sudo iptables -F`

---

## 21.7 Package Management Labs

### 21.7.1 APT (Debian/Ubuntu) Lab
21.7.1.1 Update package index: `sudo apt update`
21.7.1.2 List upgradable packages: `apt list --upgradable`
21.7.1.3 Upgrade all packages: `sudo apt upgrade`
21.7.1.4 Search for `nginx` package: `apt search nginx`
21.7.1.5 Install `htop`: `sudo apt install htop`
21.7.1.6 Show detailed info about `nginx`: `apt show nginx`
21.7.1.7 Remove `htop` but keep configs: `sudo apt remove htop`
21.7.1.8 Purge `htop` completely: `sudo apt purge htop`
21.7.1.9 List all installed packages: `apt list --installed | wc -l`
21.7.1.10 Add a PPA: `sudo add-apt-repository ppa:deadsnakes/ppa`

### 21.7.2 DNF/YUM (RHEL/CentOS) Lab
21.7.2.1 List enabled repositories: `dnf repolist`
21.7.2.2 Search for `nginx`: `dnf search nginx`
21.7.2.3 Install `tree`: `sudo dnf install tree`
21.7.2.4 Show package info: `dnf info tree`
21.7.2.5 Update all packages: `sudo dnf update`
21.7.2.6 Remove package: `sudo dnf remove tree`
21.7.2.7 View transaction history: `dnf history`
21.7.2.8 Rollback a transaction: `sudo dnf history undo <id>`
21.7.2.9 Install EPEL repository: `sudo dnf install epel-release`
21.7.2.10 List all package groups: `dnf group list`

---

## 21.8 Systemd & Service Management Labs

### 21.8.1 Service Control Lab
21.8.1.1 Check status of `ssh` service: `sudo systemctl status ssh`
21.8.1.2 Stop the `cron` service: `sudo systemctl stop cron`
21.8.1.3 Start the `cron` service: `sudo systemctl start cron`
21.8.1.4 Restart the `nginx` service (if installed)
21.8.1.5 Reload `nginx` without downtime: `sudo systemctl reload nginx`
21.8.1.6 Enable `nginx` to start at boot: `sudo systemctl enable nginx`
21.8.1.7 Disable `nginx` from boot: `sudo systemctl disable nginx`
21.8.1.8 List all active services: `systemctl list-units --type=service`
21.8.1.9 List all failed services: `systemctl --failed`
21.8.1.10 Check if service is enabled: `systemctl is-enabled ssh`

### 21.8.2 Creating a Custom Systemd Service
21.8.2.1 Create a script `/usr/local/bin/myapp.sh` that writes timestamp to log
21.8.2.2 Create service file `/etc/systemd/system/myapp.service` with `ExecStart`
21.8.2.3 Add `After=network.target` and `WantedBy=multi-user.target`
21.8.2.4 Reload systemd: `sudo systemctl daemon-reload`
21.8.2.5 Start and enable the service
21.8.2.6 Check service status and logs
21.8.2.7 Add `Restart=always` and `RestartSec=10` to service file
21.8.2.8 Add `Environment="MY_VAR=hello"` to inject environment variable
21.8.2.9 Use `User=nobody` to run service as non-root
21.8.2.10 Stop and disable the service, remove the script

### 21.8.3 Journalctl Lab
21.8.3.1 View all journal logs: `journalctl`
21.8.3.2 View logs for specific service: `journalctl -u ssh`
21.8.3.3 Follow real-time logs: `journalctl -f`
21.8.3.4 View logs from last 10 minutes: `journalctl --since "10 minutes ago"`
21.8.3.5 View logs between specific times: `journalctl --since "09:00" --until "17:00"`
21.8.3.6 View kernel logs: `journalctl -k`
21.8.3.7 Show logs with priority ERROR only: `journalctl -p err`
21.8.3.8 Show last 50 lines of SSH logs: `journalctl -u ssh -n 50`
21.8.3.9 Check disk usage of journal: `journalctl --disk-usage`
21.8.3.10 Rotate journal logs: `sudo journalctl --rotate`

---

## 21.9 Cron & Scheduling Labs

### 21.9.1 Basic Cron Lab
21.9.1.1 Open crontab for current user: `crontab -e`
21.9.1.2 Schedule a job to run every day at 2:30 AM
21.9.1.3 Schedule a job to run every Monday at 5 PM
21.9.1.4 Schedule a job to run every 15 minutes
21.9.1.5 Schedule a job to run at midnight on the first day of every month
21.9.1.6 List current crontab: `crontab -l`
21.9.1.7 Remove all cron jobs: `crontab -r`
21.9.1.8 Schedule a job that logs output to a file with timestamp
21.9.1.9 Redirect stderr to stdout in cron command
21.9.1.10 Use `@reboot` to run a script at system startup

### 21.9.2 System Cron Lab
21.9.2.1 Edit system crontab: `sudo nano /etc/crontab`
21.9.2.2 Add a job that runs as `root` user
21.9.2.3 Place a script in `/etc/cron.daily/` for daily execution
21.9.2.4 Check cron logs: `sudo tail -f /var/log/syslog | grep CRON`
21.9.2.5 Test a failing cron job and debug with email/redirect
21.9.2.6 Use `*/10 * * * *` syntax for every 10 minutes
21.9.2.7 Use `0 9-17 * * 1-5` for every hour between 9 AM and 5 PM on weekdays
21.9.2.8 Use wrapper script to ensure cron job doesn't run simultaneously
21.9.2.9 Create lock file mechanism using `flock`
21.9.2.10 Verify cron service is running: `sudo systemctl status cron`

---

## 21.10 SSH Labs

### 21.10.1 SSH Key Authentication Lab
21.10.1.1 Generate an SSH key pair (RSA 4096): `ssh-keygen -t rsa -b 4096`
21.10.1.2 Generate Ed25519 key: `ssh-keygen -t ed25519`
21.10.1.3 View public key: `cat ~/.ssh/id_rsa.pub`
21.10.1.4 Copy public key to remote server: `ssh-copy-id user@remote`
21.10.1.5 Manually add public key to `~/.ssh/authorized_keys` on remote
21.10.1.6 Set correct permissions: `chmod 600 ~/.ssh/authorized_keys`
21.10.1.7 SSH into remote server without password
21.10.1.8 Add key to `ssh-agent`: `ssh-add ~/.ssh/id_rsa`
21.10.1.9 List loaded keys: `ssh-add -l`
21.10.1.10 Remove all keys from agent: `ssh-add -D`

### 21.10.2 SSH Config Lab
21.10.2.1 Create `~/.ssh/config` file
21.10.2.2 Add host alias `devbox` with Hostname, User, Port, IdentityFile
21.10.2.3 Test connecting: `ssh devbox`
21.10.2.4 Add `ProxyJump` to connect through bastion host
21.10.2.5 Enable `ControlMaster` for connection reuse
21.10.2.6 Set `ServerAliveInterval 60` to keep connection alive
21.10.2.7 Disable password auth in `sshd_config` (for security lab)
21.10.2.8 Change SSH port to 2222 and test connection
21.10.2.9 Restart SSH daemon: `sudo systemctl restart sshd`
21.10.2.10 Use `ssh -v` to debug connection issues

### 21.10.3 SSH File Transfer & Tunneling Lab
21.10.3.1 Copy file using `scp`: `scp local.txt user@remote:/path/`
21.10.3.2 Copy directory recursively: `scp -r ./dir user@remote:/path/`
21.10.3.3 Use `rsync` to sync local to remote: `rsync -avz ./local/ user@remote:/remote/`
21.10.3.4 Use `rsync --delete` to mirror directories
21.10.3.5 Open SFTP session: `sftp user@remote`
21.10.3.6 In SFTP, use `get`, `put`, `ls`, `mkdir`, `rm`
21.10.3.7 Local port forwarding: `ssh -L 8080:localhost:80 user@remote`
21.10.3.8 Test tunnel by opening `localhost:8080` in browser
21.10.3.9 Remote port forwarding: `ssh -R 9090:localhost:22 user@remote`
21.10.3.10 Dynamic SOCKS proxy: `ssh -D 1080 user@remote`

---

## 21.11 Shell Scripting Labs

### 21.11.1 Variables and Conditionals Lab
21.11.1.1 Write script that accepts name as argument and prints "Hello, name"
21.11.1.2 Write script that checks if file exists before operating
21.11.1.3 Write script that uses `if-elif-else` to check number ranges
21.11.1.4 Write script using `case` statement for menu options
21.11.1.5 Write script that checks exit code of previous command
21.11.1.6 Write script using `&&` and `||` for conditional execution
21.11.1.7 Write script that validates user input (not empty)
21.11.1.8 Write script that uses `-z` and `-n` string tests
21.11.1.9 Write script that compares two numbers using `-eq`, `-gt`, `-lt`
21.11.1.10 Write script that checks file type: regular, directory, symlink

### 21.11.2 Loops Lab
21.11.2.1 Write `for` loop to iterate over list of servers (hostnames)
21.11.2.2 Write `for` loop to rename all `.txt` files to `.bak`
21.11.2.3 Write `while` loop reading file line by line
21.11.2.4 Write `until` loop that waits for a file to appear
21.11.2.5 Write script with `break` when condition is met
21.11.2.6 Write script with `continue` to skip certain iterations
21.11.2.7 Write nested loop to create multiplication table
11.11.2.8 Write loop over `{1..10}` range
21.11.2.9 Write loop over output of `ls` command
21.11.2.10 Write infinite loop with `sleep` and exit condition

### 21.11.3 Functions and Arrays Lab
21.11.3.1 Write function `log_message` that prints timestamped logs
21.11.3.2 Write function that accepts two arguments and returns sum
21.11.3.3 Write function that checks if command exists
21.11.3.4 Create indexed array of months and print 3rd element
21.11.3.5 Loop through array and print each element
21.11.3.6 Create associative array mapping service names to ports
21.11.3.7 Write function that returns error code (0 success, 1 failure)
21.11.3.8 Source external library file containing utility functions
21.11.3.9 Use `local` keyword to prevent variable conflicts
21.11.3.10 Write recursive function to calculate factorial

### 21.11.4 Error Handling and Debugging Lab
21.11.4.1 Write script with `set -e` to exit on error
21.11.4.2 Write script with `set -u` to catch unset variables
21.11.4.3 Write script with `set -x` to trace execution
21.11.4.4 Combine `set -euxo pipefail` for strict mode
21.11.4.5 Use `trap` to catch `SIGINT` and clean up temp files
21.11.4.6 Write script that logs errors to file and continues
21.11.4.7 Use `||` fallback when command fails
21.11.4.8 Check `$?` after critical operation
21.11.4.9 Write script that retries command 3 times before failing
21.11.4.10 Use `shellcheck` to lint your scripts

---

## 21.12 Linux for Containers Labs

### 21.12.1 Namespace Exploration Lab
21.12.1.1 Run `sudo lsns` to list all namespaces on system
21.12.1.2 Run `sleep 300` in background and find its PID
21.12.1.3 Check PID namespace: `sudo ls -la /proc/<PID>/ns/`
21.12.1.4 Run a container with Docker: `docker run -d --name test nginx`
21.12.1.5 Find container PID: `docker inspect test | grep Pid`
21.12.1.6 Compare host and container namespaces
21.12.1.7 Use `nsenter` to enter container namespace: `nsenter -t <PID> -n ip addr`
21.12.1.8 Create new network namespace: `sudo ip netns add myns`
21.12.1.9 Run command in new namespace: `sudo ip netns exec myns bash`
21.12.1.10 Delete namespace: `sudo ip netns del myns`

### 21.12.2 Cgroup Lab
21.12.2.1 View cgroups v2 mount: `mount | grep cgroup`
21.12.2.2 List cgroup controllers: `cat /proc/cgroups`
21.12.2.3 Create a cgroup for memory limit: `sudo mkdir /sys/fs/cgroup/memory/mygroup`
21.12.2.4 Set memory limit: `echo 100M | sudo tee /sys/fs/cgroup/memory/mygroup/memory.limit_in_bytes`
21.12.2.5 Add a process to cgroup: `echo <PID> | sudo tee /sys/fs/cgroup/memory/mygroup/cgroup.procs`
21.12.2.6 Run `stress` to test memory limit
21.12.2.7 Monitor memory usage from cgroup stats
21.12.2.8 Remove cgroup: `sudo rmdir /sys/fs/cgroup/memory/mygroup`
21.12.2.9 Use `docker run --memory=256m` and verify cgroup
21.12.2.10 Check container cgroup path: `docker inspect <container> | grep Cgroup`

### 21.12.3 Container Debugging Lab
21.12.3.1 Run nginx container: `docker run -d --name web nginx`
21.12.3.2 Exec into container: `docker exec -it web bash`
21.12.3.3 Check container processes from inside: `ps aux`
21.12.3.4 From host, view container logs: `docker logs web`
21.12.3.5 Inspect container details: `docker inspect web`
21.12.3.6 Copy file from container: `docker cp web:/etc/nginx/nginx.conf .`
21.12.3.7 Check container resource usage: `docker stats web`
21.12.3.8 Find container PID on host: `docker inspect web | grep Pid`
21.12.3.9 Use `nsenter` from host to debug container network
21.12.3.10 Stop and remove container: `docker stop web && docker rm web`

---

## 21.13 Performance Monitoring Labs

### 21.13.1 CPU and Load Lab
21.13.1.1 Run `uptime` and interpret load averages (1, 5, 15 min)
21.13.1.2 Use `mpstat -P ALL 2` to see per-core CPU usage
21.13.1.3 Run `stress --cpu 4` and monitor with `top`
21.13.1.4 Use `pidstat 2` to see per-process CPU statistics
21.13.1.5 Find process using most CPU: `ps aux --sort=-%cpu | head -5`
21.13.1.6 Use `perf top` to see CPU hotspots (install if needed)
21.13.1.7 Check interrupt rates: `cat /proc/interrupts`
21.13.1.8 Run `vmstat 1` and watch `us`, `sy`, `id`, `wa` columns
21.13.1.9 Check context switches: `vmstat -s | grep context`
21.13.1.10 Terminate stress test

### 21.13.2 Memory Lab
21.13.2.1 Run `free -h` and note used vs available
21.13.2.2 Use `vmstat -s` for detailed memory stats
21.13.2.3 Run `stress --vm 2 --vm-bytes 256M` in background
21.13.2.4 Monitor with `smem -p` (per-process memory)
21.13.2.5 Use `ps aux --sort=-%mem | head -10` to find memory hogs
21.13.2.6 Check OOM score of processes: `cat /proc/<PID>/oom_score`
21.13.2.7 Adjust OOM adj: `echo -500 | sudo tee /proc/<PID>/oom_score_adj`
21.13.2.8 Check swap usage: `cat /proc/swaps`
21.13.2.9 Enable/disable swap: `sudo swapoff -a && sudo swapon -a`
21.13.2.10 Clean cache and re-check memory

### 21.13.3 Disk I/O Lab
21.13.3.1 Run `iostat -x 2` to see disk utilization (`%util` column)
21.13.3.2 Use `iotop` (install if needed) to see I/O per process
21.13.3.3 Create large file: `dd if=/dev/zero of=/tmp/test bs=1M count=1000`
21.13.3.4 Monitor I/O during file creation
21.13.3.5 Use `dstat` (install) to see combined CPU, disk, network
21.13.3.6 Check disk latency: `iostat -d -x 1`
21.13.3.7 Find files with high I/O using `lsof` and `/proc`
21.13.3.8 Use `blktrace` to trace block I/O (advanced)
21.13.3.9 Check scheduler for disk: `cat /sys/block/sda/queue/scheduler`
21.13.3.10 Run `fio` for synthetic I/O benchmark

### 21.13.4 Network Performance Lab
21.13.4.1 Run `iperf3 -s` on one terminal, `iperf3 -c localhost` on another
21.13.4.2 Use `iftop` to see real-time bandwidth per connection
21.13.4.3 Use `nethogs` to see bandwidth per process
21.13.4.4 Check network stats: `netstat -i`
21.13.4.5 Use `ss -ti` to see TCP internal stats (RTT, cwnd)
21.13.4.6 Check packet drops: `netstat -s | grep -i drop`
21.13.4.7 Use `tcpdump -i eth0 -c 100` to capture packets
21.13.4.8 Analyze capture with `tcpdump -r capture.pcap | head`
21.13.4.9 Check socket buffer sizes: `sysctl net.ipv4.tcp_rmem`
21.13.4.10 Measure latency: `ping -c 10 google.com` and check min/avg/max

---

## 21.14 Log Management Labs

### 21.14.1 System Log Analysis Lab
21.14.1.1 View `/var/log/syslog` and find recent errors
21.14.1.2 View `/var/log/auth.log` and find failed SSH attempts
21.14.1.3 Use `grep` to extract all authentication failures in last hour
21.14.1.4 Use `tail -f /var/log/syslog` in one terminal and perform actions
21.14.1.5 Count unique IPs that failed SSH login: `grep "Failed password" /var/log/auth.log | awk '{print $11}' | sort | uniq -c`
21.14.1.6 View kernel log: `dmesg | tail -20`
21.14.1.7 Check boot messages: `dmesg | grep -i "error"`
21.14.1.8 Monitor real-time kernel messages: `dmesg -w`
21.14.1.9 Check package manager logs: `head /var/log/dpkg.log` (Debian) or `/var/log/yum.log` (RHEL)
21.14.1.10 Rotate logs manually: `sudo logrotate -f /etc/logrotate.conf`

### 21.14.2 logrotate Lab
21.14.2.1 Create custom logrotate config `/etc/logrotate.d/myapp`
21.14.2.2 Configure daily rotation with keep 7 days of logs
21.14.2.3 Enable compression of rotated logs
21.14.2.4 Add `delaycompress` to keep last rotation uncompressed
21.14.2.5 Use `size 10M` to rotate based on size
21.14.2.6 Add `postrotate` script to restart application after rotation
21.14.2.7 Use `missingok` to avoid errors if log missing
21.14.2.8 Use `notifempty` to skip empty logs
21.14.2.9 Test configuration: `sudo logrotate -d /etc/logrotate.d/myapp`
21.14.2.10 Force rotation: `sudo logrotate -f /etc/logrotate.d/myapp`

---

## 21.15 Security Hardening Labs

### 21.15.1 File Integrity Lab
21.15.1.1 Install `aide`: `sudo apt install aide` (Debian) or `sudo yum install aide` (RHEL)
21.15.1.2 Initialize AIDE database: `sudo aideinit`
21.15.1.3 Run first integrity check: `sudo aide --check`
21.15.1.4 Modify a system file like `/etc/hosts`
21.15.1.5 Run AIDE again to detect change
21.15.1.6 Update database after legitimate changes: `sudo aide --update`
21.15.1.7 Schedule daily AIDE checks with cron
21.15.1.8 Use `auditd` to monitor `/etc/passwd` changes
21.15.1.9 Add audit rule: `sudo auditctl -w /etc/passwd -p wa -k identity`
21.15.1.10 View audit logs: `sudo ausearch -k identity`

### 21.15.2 SSH Hardening Lab
21.15.2.1 Edit `/etc/ssh/sshd_config` to disable root login: `PermitRootLogin no`
21.15.2.2 Disable password authentication: `PasswordAuthentication no`
21.15.2.3 Change default SSH port to 2222
21.15.2.4 Allow only specific users: `AllowUsers devops_user`
21.15.2.5 Set `MaxAuthTries 3` to limit login attempts
21.15.2.6 Set `ClientAliveInterval 300` and `ClientAliveCountMax 0`
21.15.2.7 Restart SSH and test changes
21.15.2.8 Install and configure `fail2ban` for SSH protection
21.15.2.9 Check fail2ban status: `sudo fail2ban-client status sshd`
21.15.2.10 Test by failing SSH login multiple times

### 21.15.3 AppArmor/SELinux Lab (Ubuntu Example)
21.15.3.1 Check AppArmor status: `sudo aa-status`
21.15.3.2 List loaded profiles: `sudo apparmor_status`
21.15.3.3 Create simple profile for `/usr/sbin/nginx`
21.15.3.4 Put profile in complain mode: `sudo aa-complain /etc/apparmor.d/usr.sbin.nginx`
21.15.3.5 Generate logs from nginx and adjust profile
21.15.3.6 Enforce mode: `sudo aa-enforce /etc/apparmor.d/usr.sbin.nginx`
21.15.3.7 Test nginx with enforced profile
21.15.3.8 Disable profile: `sudo aa-disable /etc/apparmor.d/usr.sbin.nginx`
21.15.3.9 (RHEL) Check SELinux status: `getenforce`
21.15.3.10 (RHEL) View SELinux denials: `sudo ausearch -m avc`

---

## 21.16 Real-World Troubleshooting Labs

### 21.16.1 "High CPU Usage" Simulation
21.16.1.1 Run `stress --cpu 2 --timeout 60` to simulate high CPU
21.16.1.2 Use `top` to identify offending process
21.16.1.3 Use `htop` to kill the process
21.16.1.4 Use `ps aux --sort=-%cpu | head` to list top CPU consumers
21.16.1.5 Use `strace -p <PID>` on a busy process
21.16.1.6 Use `perf top` to see CPU functions (install if needed)
21.16.1.7 Check CPU frequency scaling: `cat /proc/cpuinfo | grep MHz`
21.16.1.8 Check for runaway process with `pidstat 1`
21.16.1.9 Use `kill -STOP` to pause process, then `-CONT` to resume
21.16.1.10 Document your investigation steps

### 21.16.2 "Disk Full" Simulation
21.16.2.1 Create 500MB file: `dd if=/dev/zero of=/tmp/bigfile bs=1M count=500`
21.16.2.2 Check disk usage: `df -h`
21.16.2.3 Find the large file using `du -sh /* 2>/dev/null | sort -h`
21.16.2.4 Simulate inode exhaustion: `for i in {1..100000}; do touch /tmp/$i; done`
21.16.2.5 Check inode usage: `df -i`
21.16.2.6 Find directory with many files: `find /tmp -type f | wc -l`
21.16.2.7 Delete small files: `find /tmp -type f -name "[0-9]*" -delete`
21.16.2.8 Simulate open deleted file: create, tail -f, delete, check `lsof`
21.16.2.9 Find deleted files still held open: `lsof | grep deleted`
21.16.2.10 Clear disk space properly without killing processes

### 21.16.3 "Port Already in Use" Simulation
21.16.3.1 Start a service on port 8080: `python3 -m http.server 8080 &`
21.16.3.2 Try to start another service on same port
21.16.3.3 Find process using port: `ss -tlnp | grep 8080`
21.16.3.4 Alternative: `lsof -i :8080`
21.16.3.5 Kill process using port: `kill -9 <PID>`
21.16.3.6 Simulate TIME_WAIT state: open connection and close quickly
21.16.3.7 Check socket reuse options: `sysctl net.ipv4.tcp_tw_reuse`
21.16.3.8 Use `netstat -tunap | grep 8080` as alternative
21.16.3.9 Use `fuser -k 8080/tcp` to kill process on port
21.16.3.10 Verify port is free and restart service

### 21.16.4 "Cannot Connect to Server" Simulation
21.16.4.1 Check if service is listening: `ss -tlnp | grep 22`
21.16.4.2 Check firewall: `sudo ufw status` or `sudo iptables -L`
21.16.4.3 Test local connectivity: `telnet localhost 22`
21.16.4.4 Check DNS resolution: `nslookup hostname`
21.16.4.5 Check routing: `ip route get <destination IP>`
21.16.4.6 Use `traceroute` to find network break
21.16.4.7 Check if service is running: `systemctl status ssh`
21.16.4.8 Check logs: `journalctl -u ssh`
21.16.4.9 Check SELinux/AppArmor blocking
21.16.4.10 Use `nc -zv host port` to test connectivity

---

## 21.17 Final Integration Lab (Putting It All Together)

### 21.17.1 Complete Server Setup from Scratch
21.17.1.1 Launch an Ubuntu VM (local or cloud)
21.17.1.2 Update package index and upgrade all packages
21.17.1.3 Create a new user `deploy` with sudo privileges
21.17.1.4 Set up SSH key authentication for `deploy` (disable password)
21.17.1.5 Install and configure `nginx` web server
21.17.1.6 Create custom `index.html` with server hostname
21.17.1.7 Set up systemd service to ensure nginx starts on boot
21.17.1.8 Configure `ufw` to allow SSH (port 22) and HTTP (80) only
21.17.1.9 Write bash script that checks nginx status every 5 minutes via cron
21.17.1.10 Set up logrotate for nginx logs (daily, keep 7 days)

### 21.17.2 Deploy a Simple Application
21.17.2.1 Install Python3 and pip
21.17.2.2 Create a Flask app that returns "Hello DevOps"
21.17.2.3 Run it as a systemd service on port 5000
21.17.2.4 Configure nginx as reverse proxy to port 5000
21.17.2.5 Test the application via browser/curl
21.17.2.6 Set up `prometheus-node-exporter` to monitor server
21.17.2.7 Write script to check disk usage and send alert to syslog if > 80%
21.17.2.8 Automate backup of `/etc/nginx` to `/backup/nginx-$(date +%Y%m%d).tar.gz`
21.17.2.9 Schedule backup daily at 2 AM
21.17.2.10 Document all steps in a shell script for repeatability

