# Linux For DevOps (Complete Syllabus)


## 📋 Linux Cheatsheet Quick Reference

File & Directory Operations
  - [List (ls)](linux-cheetsheet.md#list-ls)
  - [Change Directory (cd)](linux-cheetsheet.md#change-directory-cd)
  - [Make Directory (mkdir)](linux-cheetsheet.md#make-directory-mkdir)
  - [Remove (rm)](linux-cheetsheet.md#remove-rm)
  - [Copy (cp)](linux-cheetsheet.md#copycp)
  - [Move (mv)](linux-cheetsheet.md#move-mv)
  - [Link (ln)](linux-cheetsheet.md#link-ln)

File Viewing & Inspection
  - [Cat (concatenate)](linux-cheetsheet.md#cat-concatenate)
  - [Paged File Viewing](linux-cheetsheet.md#paged-file-viewing)
  - [Beginning & End of Files](linux-cheetsheet.md#beginning--end-of-files)
  - [Determining File Content Type (file)](linux-cheetsheet.md#determining-file-content-type-file)

Permissions & Ownership
  - [Changing File and Directory Permissions (chmod)](linux-cheetsheet.md#changing-file-and-directory-permissions-chmod)
  - [Changing File and Directory Ownership (chown)](linux-cheetsheet.md#changing-file-and-directory-ownership-chown)
  - [Changing Group Ownership (chgrp)](linux-cheetsheet.md#changing-group-ownership-chgrp)
  - [SUID (4), SGID (2), Sticky Bit (1)](linux-cheetsheet.md#suid-4--sgid-2--sticky-bit-1)
  - [Managing Default File Creation Permissions (umask)](linux-cheetsheet.md#managing-default-file-creation-permissions-umask)
  - [Managing Access Control Lists (getfacl, setfacl)](linux-cheetsheet.md#managing-access-control-lists-getfacl-setfacl)

Finding Files & Directories
  - [Finding Files and Directories (find)](linux-cheetsheet.md#finding-files-and-directories-find)
  - [Updating and Searching the File Database (updatedb / locate)](linux-cheetsheet.md#updating-and-searching-the-file-database-updatedb--locate)

Searching Text Inside Files [Global Regular Expression Print (grep)]
  - [Basic Text Matching](linux-cheetsheet.md#basic-text-matching)
  - [Recursive and Location Matching](linux-cheetsheet.md#recursive-and-location-matching)
  - [Output Customization and Formatting](linux-cheetsheet.md#output-customization-and-formatting)
  - [Context-Based Matching](linux-cheetsheet.md#context-based-matching)

Process Management
  - [Viewing and Monitoring Processes](linux-cheetsheet.md#viewing-and-monitoring-processes)
  - [Searching and Tracking Processes](linux-cheetsheet.md#searching-and-tracking-processes)
  - [Finding Resource and Port Locks](linux-cheetsheet.md#finding-resource-and-port-locks)
  - [Termination and Signals](linux-cheetsheet.md#termination-and-signals)
  - [Process Priority (Nice Levels)](linux-cheetsheet.md#process-priority-nice-levels)
  - [Background and Foreground Jobs](linux-cheetsheet.md#background-and-foreground-jobs)
  - [Finding Shell Process IDs](linux-cheetsheet.md#finding-shell-process-ids)
  - [Finding Parent Process Details](linux-cheetsheet.md#finding-parent-process-details)
  - [Tracing System Calls and Processes (strace)](linux-cheetsheet.md#tracing-system-calls-and-processes-strace)

Memory & Disk Management
  - [Monitoring System Memory](linux-cheetsheet.md#monitoring-system-memory)
  - [Real-Time Resource and Performance Monitoring](linux-cheetsheet.md#real-time-resource-and-performance-monitoring)
  - [Clearing System Caches](linux-cheetsheet.md#clearing-system-caches)
  - [Managing Swap Space (swapon, swapoff)](linux-cheetsheet.md#managing-swap-space-swapon-swapoff)
  - [Monitoring Disk Space Usage](linux-cheetsheet.md#monitoring-disk-space-usage)
  - [Listing and Managing Storage Devices](linux-cheetsheet.md#listing-and-managing-storage-devices)

User & Group Administration
  - [Creating and Deleting](linux-cheetsheet.md#creating-and-deleting)
  - [Modifying Existing User Accounts](linux-cheetsheet.md#modifying-existing-user-accounts)
  - [Securing User Accounts and Password Policies](linux-cheetsheet.md#securing-user-accounts-and-password-policies)
  - [Customizing Account and Password Aging](linux-cheetsheet.md#customizing-account-and-password-aging)
  - [Switching User Sessions (su, sudo)](linux-cheetsheet.md#switching-user-sessions-su-sudo)
  - [Creating, Deleting, and Modifying Groups](linux-cheetsheet.md#creating-deleting-and-modifying-groups)
  - [Inspecting User Login History](linux-cheetsheet.md#inspecting-user-login-history)
  - [Auditing Active Users and Groups](linux-cheetsheet.md#auditing-active-users-and-groups)
  - [Inspecting System Configuration Files](linux-cheetsheet.md#inspecting-system-configuration-files)
  - [Editing and Verifying System Privilege Rules](linux-cheetsheet.md#editing-and-verifying-system-privilege-rules)

Services & Systemd
  - [Controlling Service Runtime States](linux-cheetsheet.md#controlling-service-runtime-states)
  - [Configuring Automatic Service Boot Behaviors](linux-cheetsheet.md#configuring-automatic-service-boot-behaviors)
  - [Inspecting Service and System States](linux-cheetsheet.md#inspecting-service-and-system-states)
  - [Auditing Service Activity Logs (journalctl)](linux-cheetsheet.md#auditing-service-activity-logs-journalctl)

Cron & Task Scheduling
  - [Managing User Cron Tables (crontab)](linux-cheetsheet.md#managing-user-cron-tables-crontab)
  - [Managing Rules for Other Users](linux-cheetsheet.md#managing-rules-for-other-users)
  - [Auditing System-Wide Tasks and Schedules](linux-cheetsheet.md#auditing-system-wide-tasks-and-schedules)
  - [Managing Access Restriction Rules](linux-cheetsheet.md#managing-access-restriction-rules)

Archiving and Compressing Files (tar)
  - [Creating Archives](linux-cheetsheet.md#creating-archives)
  - [Extracting Archives](linux-cheetsheet.md#extracting-archives)
  - [Inspecting and Filtering](linux-cheetsheet.md#inspecting-and-filtering)


---


## 1. LINUX FUNDAMENTALS (CORE CONCEPTS)

[1.1 What is Linux & Why DevOps Uses It](linux-syllabus.md#11-what-is-linux--why-devops-uses-it)

[1.2 Linux Distributions for DevOps](linux-syllabus.md#12-linux-distributions-for-devops)

[1.3 Filesystem Hierarchy Standard (FHS)](linux-syllabus.md#13-filesystem-hierarchy-standard-fhs)

## 2. ESSENTIAL LINUX COMMANDS (DAY-TO-DAY OPS)

[2.1 File & Directory Operations](linux-syllabus.md#21-file--directory-operations)

[2.2 File Viewing & Inspection](linux-syllabus.md#22-file-viewing--inspection)

[2.3 File Permissions & Ownership](linux-syllabus.md#23-file-permissions--ownership)

[2.4 Finding Files & Directories](linux-syllabus.md#24-finding-files--directories)

## 3. TEXT PROCESSING & STREAM EDITING (DEVOPS CORE SKILLS)

[3.1 grep (Global Regular Expression Print)](linux-syllabus.md#31-grep-global-regular-expression-print)

[3.2 sed (Stream Editor)](linux-syllabus.md#32-sed-stream-editor)

[3.3 awk (Pattern Scanning & Processing)](linux-syllabus.md#33-awk-pattern-scanning--processing)

[3.4 cut, sort, uniq, tr](linux-syllabus.md#34-cut-sort-uniq-tr)

[3.5 diff, comm, patch](linux-syllabus.md#35-diff-comm-patch)

[3.6 Regular Expressions Deep Dive](linux-syllabus.md#36-regular-expressions-deep-dive)

## 4. PROCESS MANAGEMENT

[4.1 Viewing Processes](linux-syllabus.md#41-viewing-processes)

[4.2 Managing Processes](linux-syllabus.md#42-managing-processes)

[4.3 Process Monitoring & Troubleshooting](linux-syllabus.md#43-process-monitoring--troubleshooting)

## 5. MEMORY & DISK MANAGEMENT

[5.1 Memory Monitoring](linux-syllabus.md#51-memory-monitoring)

[5.2 Disk Usage & Analysis](linux-syllabus.md#52-disk-usage--analysis)

[5.3 Logical Volume Manager (LVM)](linux-syllabus.md#53-logical-volume-manager-lvm)

## 6. USER & GROUP ADMINISTRATION

[6.1 User Management](linux-syllabus.md#61-user-management)

[6.2 Group Management](linux-syllabus.md#62-group-management)

[6.3 Sudo (Superuser Do)](linux-syllabus.md#63-sudo-superuser-do)

## 7. NETWORKING FUNDAMENTALS

[7.1 Network Configuration](linux-syllabus.md#71-network-configuration)

[7.2 Network Inspection & Debugging](linux-syllabus.md#72-network-inspection--debugging)

[7.3 Port & Connection Analysis](linux-syllabus.md#73-port--connection-analysis)

[7.4 Firewall Management](linux-syllabus.md#74-firewall-management)

## 8. PACKAGE MANAGEMENT

[8.1 APT (Debian/Ubuntu Family)](linux-syllabus.md#81-apt-debianubuntu-family)

[8.2 YUM/DNF (RHEL/CentOS/Rocky Family)](linux-syllabus.md#82-yumdnf-rhelcentosrocky-family)

[8.3 Managing Repositories & GPG Keys](linux-syllabus.md#83-managing-repositories--gpg-keys)

## 9. SERVICES & SYSTEMD

[9.1 systemd Fundamentals](linux-syllabus.md#91-systemd-fundamentals)

[9.2 Service Management](linux-syllabus.md#92-service-management)

[9.3 systemd Journal (Logging)](linux-syllabus.md#93-systemd-journal-logging)

[9.4 systemd Timers (Cron Replacement)](linux-syllabus.md#94-systemd-timers-cron-replacement)

## 10. CRON & TASK SCHEDULING

[10.1 Cron Fundamentals](linux-syllabus.md#101-cron-fundamentals)

[10.2 Advanced Cron Patterns](linux-syllabus.md#102-advanced-cron-patterns)

[10.3 Cron Troubleshooting & Best Practices](linux-syllabus.md#103-cron-troubleshooting--best-practices)

## 11. SHELL SCRIPTING (BASH FOR DEVOPS)

[11.1 Script Basics](linux-syllabus.md#111-script-basics)

[11.2 Conditional Statements](linux-syllabus.md#112-conditional-statements)

[11.3 Loops & Iteration](linux-syllabus.md#113-loops--iteration)

[11.4 Functions](linux-syllabus.md#114-functions)

[11.5 Arrays & Data Structures](linux-syllabus.md#115-arrays--data-structures)

[11.6 Exit Codes & Error Handling](linux-syllabus.md#116-exit-codes--error-handling)

[11.7 Real-World DevOps Scripting Patterns](linux-syllabus.md#117-real-world-devops-scripting-patterns)

## 12. SSH (SECURE SHELL)

[12.1 SSH Fundamentals](linux-syllabus.md#121-ssh-fundamentals)

[12.2 Key-Based Authentication](linux-syllabus.md#122-key-based-authentication)

[12.3 SSH Configuration](linux-syllabus.md#123-ssh-configuration)

[12.4 Secure File Transfer](linux-syllabus.md#124-secure-file-transfer)

[12.5 SSH Tunneling & Port Forwarding](linux-syllabus.md#125-ssh-tunneling--port-forwarding)

## 13. ARCHIVING & COMPRESSION

[13.1 tar (Tape Archive)](linux-syllabus.md#131-tar-tape-archive)

[13.2 Compression Tools](linux-syllabus.md#132-compression-tools)

[13.3 Real-World Backup Patterns](linux-syllabus.md#133-real-world-backup-patterns)

## 14. ENVIRONMENT VARIABLES & PATH

[14.1 Environment vs Shell Variables](linux-syllabus.md#141-environment-vs-shell-variables)

[14.2 Important Environment Variables](linux-syllabus.md#142-important-environment-variables)

[14.3 Shell Configuration Files](linux-syllabus.md#143-shell-configuration-files)

## 15. LINUX FOR CONTAINERS (DOCKER & KUBERNETES CONTEXT)

[15.1 Linux Features Enabling Containers](linux-syllabus.md#151-linux-features-enabling-containers)

[15.2 Container Runtime Interaction](linux-syllabus.md#152-container-runtime-interaction)

[15.3 Linux Debugging in Container Context](linux-syllabus.md#153-linux-debugging-in-container-context)

## 16. PERFORMANCE MONITORING & TROUBLESHOOTING

[16.1 System Performance Tools](linux-syllabus.md#161-system-performance-tools)

[16.2 Network Performance](linux-syllabus.md#162-network-performance)

[16.3 Common Performance Issues](linux-syllabus.md#163-common-performance-issues)

## 17. LINUX SECURITY HARDENING (FOR DEVOPS)

[17.1 System Hardening Basics](linux-syllabus.md#171-system-hardening-basics)

[17.2 File Integrity & Auditing](linux-syllabus.md#172-file-integrity--auditing)

[17.3 SELinux & AppArmor](linux-syllabus.md#173-selinux--apparmor)

## 18. LOG MANAGEMENT & ANALYSIS

[18.1 System Logs Locations](linux-syllabus.md#181-system-logs-locations)

[18.2 Log Rotation](linux-syllabus.md#182-log-rotation)

[18.3 Centralized Logging for DevOps](linux-syllabus.md#183-centralized-logging-for-devops)

## 19. LINUX FOR CLOUD & INFRASTRUCTURE AS CODE

[19.1 Cloud-Init & User Data](linux-syllabus.md#191-cloud-init--user-data)

[19.2 Configuration Management (Agent vs Agentless)](linux-syllabus.md#192-configuration-management-agent-vs-agentless)

[19.3 Linux in CI/CD Pipelines](linux-syllabus.md#193-linux-in-cicd-pipelines)

## 20. COMMON TROUBLESHOOTING SCENARIOS (INTERVIEW FOCUS)

[20.1 "High CPU usage on a Linux server"](linux-syllabus.md#201-high-cpu-usage-on-a-linux-server)

[20.2 "Disk full error but `df` shows space available"](linux-syllabus.md#202-disk-full-error-but-df-shows-space-available)

[20.3 "Port already in use but no process listening"](linux-syllabus.md#203-port-already-in-use-but-no-process-listening)

[20.4 "Cannot SSH to server"](linux-syllabus.md#204-cannot-ssh-to-server)

[20.5 "Command not found for newly installed package"](linux-syllabus.md#205-command-not-found-for-newly-installed-package)

## 21. HANDS-ON LABS (DO THESE ON YOUR TERMINAL)

[21.1 Filesystem & File Operations Labs](linux-syllabus.md#211-filesystem--file-operations-labs)

[21.2 Text Processing Labs](linux-syllabus.md#212-text-processing-labs)

[21.3 Process Management Labs](linux-syllabus.md#213-process-management-labs)

[21.4 Memory & Disk Management Labs](linux-syllabus.md#214-memory--disk-management-labs)

[21.5 User & Group Administration Labs](linux-syllabus.md#215-user--group-administration-labs)

[21.6 Networking Labs](linux-syllabus.md#216-networking-labs)

[21.7 Package Management Labs](linux-syllabus.md#217-package-management-labs)

[21.8 Systemd & Service Management Labs](linux-syllabus.md#218-systemd--service-management-labs)

[21.9 Cron & Scheduling Labs](linux-syllabus.md#219-cron--scheduling-labs)

[21.10 SSH Labs](linux-syllabus.md#2110-ssh-labs)

[21.11 Shell Scripting Labs](linux-syllabus.md#2111-shell-scripting-labs)

[21.12 Linux for Containers Labs](linux-syllabus.md#2112-linux-for-containers-labs)

[21.13 Performance Monitoring Labs](linux-syllabus.md#2113-performance-monitoring-labs)

[21.14 Log Management Labs](linux-syllabus.md#2114-log-management-labs)

[21.15 Security Hardening Labs](linux-syllabus.md#2115-security-hardening-labs)

[21.16 Real-World Troubleshooting Labs](linux-syllabus.md#2116-real-world-troubleshooting-labs)

[21.17 Final Integration Lab (Putting It All Together)](linux-syllabus.md#2117-final-integration-lab-putting-it-all-together)
