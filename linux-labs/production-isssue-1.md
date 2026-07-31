# 1. Process Management Issues

## Question 1
### Application is completely unresponsive/stuck

Users report that the application has suddenly become unresponsive, and all incoming requests are timing out. The process is still visible in the system and appears to be running, but it is no longer responding to user requests or accepting new connections. The issue started unexpectedly, and business operations are currently affected. How do you diagnose and resolve the problem?

---

## Question 2
### Process is using 100% CPU

A production server is experiencing severe performance degradation because one application process is continuously consuming nearly 100% CPU. Other applications running on the same server have become slow and users are reporting delayed responses. Determine the root cause of the high CPU utilization and restore normal system performance.

---

## Question 3
### Process memory continuously increasing (Memory Leak)

An application has been running for several hours, and its memory consumption continues to increase without dropping back to normal levels. Eventually, the server starts experiencing memory pressure and overall performance begins to degrade. There are no obvious error messages in the application logs. How would you investigate and resolve the suspected memory leak?

---

## Question 4
### Application crashes with "Too Many Open Files" (EMFILE)

A production application runs normally for some time but eventually crashes with an error indicating that too many files are open. After restarting the application, it works again temporarily before the same issue reappears. Users are unable to access the service whenever the crash occurs. How would you identify the cause and prevent the problem from happening again?

---

## Question 5
### Process consuming excessive memory causing swapping and OOM Killer

One application is consuming an unusually large amount of memory, causing the system to use swap heavily. Eventually, the Linux Out Of Memory (OOM) Killer terminates one or more processes to recover memory. Critical services become unavailable after the incident. How would you diagnose the issue and restore system stability?

---

## Question 6
### Zombie processes accumulating

The number of zombie processes on the server continues to increase over time. Although they consume very little memory, administrators notice that the process table is gradually filling up, raising concerns about system stability. The parent application is still running. How would you investigate the cause and eliminate the zombie processes?

---

## Question 7
### Background job terminates after SSH logout

A long-running maintenance script is started from an SSH session and appears to be executing correctly. However, immediately after the administrator disconnects from the server, the process terminates before completing its work. This behavior has caused multiple failed maintenance operations. How would you ensure that such jobs continue running even after the SSH session ends?

---

## Question 8
### Need to detach a foreground process without stopping it

An administrator starts a backup process directly from the terminal without running it in the background. The operation is expected to take several hours, but the administrator now needs to close the terminal and continue working elsewhere. Restarting the backup would waste significant time. How would you detach the running process without interrupting it?

---

## Question 9
### Application won't start because the required port is already in use

A newly deployed application fails to start and immediately reports that the required network port is already occupied. The service was functioning correctly before the deployment, and another process appears to be using the same port. As a result, the new application cannot begin accepting client requests. How would you identify the conflict and restore the service?

---

## Question 10
### Process won't terminate with a normal kill command

An application becomes unresponsive and administrators attempt to terminate it using the standard kill command. Despite multiple attempts, the process remains active and continues consuming system resources. Other services depending on it are also affected. How would you investigate why the process cannot be terminated and safely recover the system?

---

## Question 11
### Process priority is too low or too high

A critical production application is either receiving insufficient CPU time or monopolizing CPU resources compared to other processes on the server. Users report inconsistent performance depending on system load. The issue appears to be related to process scheduling priority. How would you identify the problem and adjust the process priority appropriately?

---

## Question 12
### Child processes not terminating with parent process

A parent application has been stopped successfully, but several child processes continue running independently. These orphaned processes continue consuming system resources and may interfere with future application restarts. Administrators need to ensure proper cleanup of all related processes. How would you investigate and resolve the issue?

---

## Question 13
### Unable to locate a process by name

Users report that an application is running, but administrators are unable to locate its process using the expected process name. The application may have been started under a different executable name, by another user, or through a service manager. Without identifying the correct process, further troubleshooting cannot continue. How would you locate the process?

---

## Question 14
### Application crashes immediately after startup

A production application starts successfully but exits almost immediately without becoming available to users. Every restart results in the same behavior, and only limited information is displayed on the console. The service remains unavailable, impacting dependent systems. How would you investigate the startup failure and determine the root cause?

---

## Question 15
### Process is running but not responding to network requests

Monitoring tools indicate that the application process is running normally, and there are no signs that it has crashed. However, clients cannot connect to the service and every request either times out or fails. From the user's perspective, the application appears to be offline even though the process is active. How would you determine why the application is not responding to network traffic?


---


## Question 16
### System load is high but CPU usage is low

Users report that the server has become extremely slow, and the system load average has increased significantly. Surprisingly, CPU utilization remains relatively low, leaving administrators unsure about the cause of the slowdown. Multiple applications hosted on the server are experiencing delayed responses. How would you investigate the reason for the high system load and restore normal performance?

---

## Question 17
### Systemd service fails to start

A critical application managed by systemd refuses to start after a routine restart. Every attempt to start the service ends in failure, preventing users from accessing the application. The service had been functioning correctly before the incident. How would you investigate the startup failure and restore the service?

---

## Question 18
### Systemd service is not restarting automatically after crash

A production service unexpectedly crashes due to an application error. Although the application has terminated, it is not automatically restarting, resulting in extended downtime until manual intervention occurs. High availability requirements demand that the service recover automatically whenever possible. How would you identify the reason and ensure automatic recovery?

---

## Question 19
### Unable to kill a process owned by another user

A runaway process owned by another user is consuming excessive system resources and affecting overall server performance. Attempts to terminate the process using normal user privileges fail due to insufficient permissions. The issue must be resolved without disrupting unrelated services. How would you safely terminate the process and verify that it does not reappear unexpectedly?

---

## Question 20
### Cron job process is not completing

A scheduled cron job starts at the expected time but never completes successfully. The task either hangs indefinitely or terminates before finishing, causing scheduled maintenance operations to fail repeatedly. This has begun affecting downstream processes that depend on its successful completion. How would you determine why the cron job is failing and restore normal execution?

---

## Question 21
### Process hierarchy appears different than expected

While investigating a production issue, you notice that the application's process hierarchy is different from what the deployment documentation describes. Some processes appear under unexpected parent processes, while others seem to have been re-parented entirely. This unusual process structure raises concerns about the application's behavior. How would you investigate the process hierarchy and determine whether it is operating correctly?

---

## Question 22
### nohup.out is growing too large

A long-running background application was started using `nohup`, and over time the `nohup.out` file has grown to several gigabytes in size. The excessive log file is consuming valuable disk space and may eventually impact other applications on the server. Administrators need to control log growth without interrupting the running process. How would you resolve the issue and prevent it from happening again?

---

## Question 23
### Process is not releasing file locks

An application has finished processing its workload, but other applications are still unable to access the affected files because they remain locked. Multiple users report that operations requiring those files are blocked, even though the original task appears to have completed. The issue is disrupting normal business operations. How would you identify the process holding the locks and safely release them?

---

## Question 24
### strace is producing too much output

While troubleshooting an application issue, you attach `strace` to a running process. The tool immediately begins generating thousands of system calls per second, making it extremely difficult to locate the information relevant to the problem. Important events are buried within the massive amount of output. How would you reduce the output to focus only on the system calls needed for your investigation?

---

## Question 25
### Unable to debug a process running as another user

A production application is running under a dedicated service account, and you need to investigate its runtime behavior. However, your current user account does not have permission to attach debugging tools to the process. The application cannot be stopped because it is actively serving production traffic. How would you gain the necessary access and perform the investigation safely?

---

# 2. File System & Storage Issues

## Question 26
### Disk is full but df shows space available

Users report that applications can no longer write data because the system claims the disk is full. However, when checking disk usage, the `df` command indicates that sufficient free space is still available. The inconsistent information is preventing administrators from identifying the actual cause of the storage problem. How would you investigate and resolve this situation?

---

## Question 27
### Disk is full due to large log files

A production server has stopped accepting new data because the filesystem has reached 100% utilization. Investigation reveals that one or more application log files have grown continuously over several weeks without rotation. Critical services are beginning to fail due to the lack of available disk space. How would you safely recover disk space and prevent the problem from recurring?

---

## Question 28
### Cannot delete file with "Device or resource busy"

An administrator attempts to remove a file that is no longer needed, but every deletion attempt fails with a "Device or resource busy" error. The file appears to be in use even though no active work is expected. The inability to remove the file is delaying maintenance activities. How would you determine why the file is busy and safely remove it?

---

## Question 29
### File permissions are incorrect after backup restoration

After restoring application data from a backup, users discover that the application can no longer access its files correctly. Several files and directories have unexpected ownership or permission settings, causing service failures and access errors. The restored data appears intact, but normal operations cannot continue. How would you identify the permission issues and restore the correct access controls?

---

## Question 30
### Filesystem unexpectedly becomes read-only

A production server suddenly begins reporting write failures across multiple applications. Administrators discover that the affected filesystem has switched into read-only mode, preventing any new data from being written. Business operations relying on that storage have effectively stopped. How would you investigate the reason for the read-only state and safely recover the filesystem?



---


## Question 31
### Cannot unmount filesystem because it's busy

An administrator attempts to unmount a filesystem before performing maintenance, but the operation repeatedly fails because the device is reported as busy. No obvious file operations are in progress, yet the filesystem remains in use. Maintenance cannot continue until the filesystem is safely unmounted. How would you identify the processes using the filesystem and complete the operation without causing data loss?

---

## Question 32
### NFS mount is stuck or hanging

Applications that rely on a mounted NFS share suddenly become unresponsive, and file operations either hang indefinitely or take an unusually long time to complete. Users are unable to read or write files stored on the network filesystem, affecting multiple services. The NFS mount itself appears to be stuck. How would you investigate the cause and restore normal access?

---

## Question 33
### Filesystem has run out of inodes

Users are unable to create new files even though disk usage reports show that plenty of storage space is still available. Applications begin failing with errors indicating that files cannot be created, causing confusion among administrators. The issue is affecting only one filesystem. How would you determine the cause and restore the ability to create new files?

---

## Question 34
### Filesystem performance is extremely slow

File operations such as reading, writing, copying, and listing directories have become noticeably slower than usual. Applications relying on the affected storage are experiencing delays, leading to increased response times and user complaints. There are no immediate signs of hardware failure, but the overall storage performance has degraded significantly. How would you investigate and identify the root cause?

---

## Question 35
### Corrupted filesystem

Following an unexpected power outage, the server fails to access files stored on a critical filesystem. Several applications cannot start because required files are either inaccessible or reported as corrupted. Administrators suspect filesystem corruption and need to recover the system while minimizing data loss. How would you approach the recovery process?

---

## Question 36
### Files disappeared after fsck

A filesystem check was performed to repair disk corruption, and the system is now operational again. However, users report that several important files and directories are missing after the repair. Business applications depending on those files are no longer functioning correctly. How would you investigate what happened and attempt to recover the missing data?

---

## Question 37
### Hard link count mismatch on a file

During a routine filesystem consistency check, administrators notice that the hard link count of a file does not match the expected value. Although the file remains accessible, the inconsistency raises concerns about filesystem integrity and possible corruption. Further investigation is required before the issue affects production workloads. How would you determine the cause of the mismatch?

---

## Question 38
### Cannot change file ownership even with sudo

An administrator attempts to change the ownership of a file using elevated privileges, but the operation repeatedly fails despite having root access. The inability to modify ownership is preventing an application from functioning correctly after migration. There are no obvious permission errors on the file itself. How would you identify what is preventing the ownership change?

---

## Question 39
### Files showing incorrect timestamps

Several application files display timestamps that are significantly different from the actual time they were created or modified. This inconsistency is making it difficult to troubleshoot recent deployments and determine the correct sequence of events. Multiple users have reported confusion when reviewing logs and application data. How would you investigate and correct the timestamp issue?

---

## Question 40
### Cannot remove directory due to permission denied

An administrator needs to remove an old application directory that is no longer required, but every attempt fails with a permission denied error. Even though the directory appears to belong to the correct user, it cannot be deleted. The leftover directory is preventing a clean deployment of the new application version. How would you determine the cause and safely remove it?

---

## Question 41
### File not found immediately after creation

An application reports that it has successfully created a file, but moments later the same file cannot be located by users or other processes. Repeating the operation produces the same unexpected behavior, making it appear as though the file disappears immediately after being created. This issue is affecting normal application workflows. How would you investigate where the file is going and why it cannot be found?

---

## Question 42
### User quota exceeded

A user reports that they are no longer able to save files or upload data to the server. Every write operation fails even though the filesystem still has available storage capacity. Other users continue working normally without any issues. How would you determine whether storage quotas are responsible and restore the user's ability to write data?

---

## Question 43
### Large number of small files causing performance issues

An application generates millions of very small files within a single directory over time. Although each file occupies very little space, overall filesystem performance has degraded significantly, and directory operations have become increasingly slow. Backup and maintenance tasks are also taking much longer than expected. How would you investigate and improve the storage performance?

---

## Question 44
### rm -rf is taking too long

An administrator attempts to delete a directory containing a massive number of files using `rm -rf`, but the operation progresses extremely slowly and appears to take several hours. The delay is preventing planned maintenance and delaying new deployments. The directory must be removed as efficiently as possible without compromising filesystem integrity. How would you approach the problem?

---

## Question 45
### File appears as binary instead of text

A configuration file that should contain readable text suddenly appears as unreadable binary data when opened. The application depending on the file fails to start because it can no longer interpret the contents correctly. Administrators are unsure whether the file has been corrupted, encoded differently, or accidentally overwritten. How would you investigate the issue and restore the correct file format?


---


## Question 46
### Symbolic link pointing to the wrong location

An application suddenly fails to access a required file, even though the symbolic link appears to exist. Further investigation reveals that the symlink is pointing to an incorrect or outdated location following a deployment or directory reorganization. As a result, the application cannot locate the required resources and users are experiencing service failures. How would you identify the incorrect symbolic link and restore the application?

---

## Question 47
### File compression is taking too long

A scheduled backup job is taking much longer than expected because compressing a large amount of data has become a bottleneck. The extended runtime is delaying backup completion and impacting other maintenance tasks that depend on it. Administrators need to improve backup performance while maintaining data integrity. How would you investigate the slowdown and determine a more efficient approach?

---

## Question 48
### Duplicate files consuming disk space

A storage server is gradually running out of space, and administrators suspect that duplicate copies of files are consuming a significant portion of the filesystem. The duplicate files have accumulated over months due to repeated backups and manual copying by different users. Before reclaiming storage, administrators need to ensure that important data is not accidentally removed. How would you identify the duplicate files and safely recover disk space?

---

## Question 49
### File permissions keep getting reset

Application files repeatedly return to incorrect ownership or permission settings shortly after being corrected. The unexpected permission changes eventually prevent the application from reading or writing its own files, resulting in intermittent service failures. Administrators suspect that another process or scheduled task is modifying the permissions automatically. How would you identify the source of the changes and permanently resolve the issue?

---

## Question 50
### rsync is not syncing files correctly

A scheduled file synchronization job using `rsync` completes without reporting major errors, but users notice that several files are missing or outdated on the destination server. Some files are transferred successfully while others appear to be skipped unexpectedly. The inconsistency is causing differences between the source and destination systems. How would you investigate why the synchronization is incomplete and ensure that both systems contain identical data?

---

# 3. Permission & Security Issues

## Question 51
### Application cannot write to files even with 777 permissions

An application is unable to create or modify files even though the affected directories have been assigned full read, write, and execute permissions. Administrators have verified the standard Linux permission bits, yet the problem persists across multiple attempts. The application continues to fail with permission-related errors, preventing normal operation. How would you determine what is blocking file access?

---

## Question 52
### Cannot execute a file even though execute permission exists

A script or executable has the correct execute permission set, but every attempt to run it results in an execution failure. The same file worked correctly on another server, suggesting that the issue is specific to the current environment. Administrators must determine why execution is being blocked before the application can be deployed. How would you investigate the problem?

---

## Question 53
### User cannot use sudo

A user who previously performed administrative tasks successfully is now unable to execute commands using `sudo`. Every attempt results in an authorization failure, preventing the user from completing routine system administration tasks. Other users with administrative privileges continue to work normally. How would you determine why the user's elevated access has stopped working and restore the required privileges?

---

## Question 54
### Incorrect ownership causing service failures

Following a migration or deployment, an application service repeatedly fails to start because it cannot access the files required for normal operation. Initial inspection shows that the necessary files exist, but they are owned by the wrong user or group. As a result, the service is unable to read configuration files or write application data. How would you identify the ownership issue and restore the service?

---

## Question 55
### SUID bit is set but elevated privileges are not applied

An executable has the SUID permission configured, yet users report that it behaves exactly like a normal program without obtaining the expected elevated privileges. The application previously worked correctly, but recent changes have caused the privilege escalation mechanism to stop functioning. This issue is preventing users from completing tasks that depend on the executable. How would you determine why the SUID behavior is not working?

---

## Question 56
### SGID not applied to newly created files

A shared project directory is configured so that all newly created files should inherit the same group ownership. However, users discover that recently created files belong to different groups, causing collaboration and permission problems. The inconsistent ownership has begun disrupting shared workflows across multiple team members. How would you investigate why the expected group inheritance is not occurring?

---

## Question 57
### ACLs overriding standard permissions

Users are confused because files appear to have the correct Linux permission bits, yet access is still denied or unexpectedly granted to certain users. The behavior is inconsistent with what administrators expect based on the traditional owner, group, and other permissions. The unexpected access control is affecting multiple shared directories. How would you determine whether Access Control Lists (ACLs) are responsible and manage them correctly?

---

## Question 58
### Sticky bit not preventing file deletion

A shared directory is intended to allow multiple users to create files while preventing them from deleting files owned by others. Despite the sticky bit being configured, users are still able to remove files that do not belong to them. This unexpected behavior raises concerns about data protection within the shared workspace. How would you investigate why the sticky bit is not providing the expected protection?

---

## Question 59
### Password policy is not being enforced

An organization recently introduced stricter password requirements, but administrators notice that users are still able to create weak passwords that do not meet the expected security standards. This creates a compliance and security concern across multiple systems. Administrators need to determine why the configured policy is not taking effect. How would you investigate and enforce the required password policy?

---

## Question 60
### User account locked after multiple failed login attempts

A user contacts the support team after being locked out of their account following several unsuccessful login attempts. The account is required for critical business operations, and the user can no longer authenticate even with the correct password. Administrators need to restore access while ensuring that the lockout occurred for legitimate security reasons. How would you investigate the lockout and safely restore access?


---




## Question 61
### Sudoers syntax error preventing sudo

A recent modification to the sudo configuration was made to grant additional administrative privileges. Shortly afterward, all users lost the ability to execute commands with `sudo`, including system administrators. Routine administration has become impossible because elevated privileges are no longer available. How would you investigate the configuration issue and safely restore administrative access?

---

## Question 62
### SELinux is blocking the application

A production application functions correctly when SELinux is disabled but immediately encounters permission-related failures when SELinux is enforcing. Standard Linux permissions appear to be configured correctly, yet the application still cannot access required resources. The organization requires SELinux to remain enabled for security compliance. How would you determine whether SELinux is responsible and restore application functionality without reducing security?

---

## Question 63
### ACLs disappear after backup and restore

A shared directory contains carefully configured Access Control Lists (ACLs) that allow multiple teams to collaborate securely. After restoring the data from a backup, users discover that the ACL entries have disappeared, resulting in unexpected permission issues across the environment. The restored files exist, but access control no longer matches the original configuration. How would you determine why the ACLs were lost and ensure they are preserved during future backups?

---

## Question 64
### Umask not working as expected

Administrators notice that newly created files consistently receive permissions different from the organization's security policy. Although the expected umask value appears to be configured, users continue creating files with incorrect default permissions. This inconsistency creates unnecessary security risks and administrative overhead. How would you investigate why the expected umask settings are not being applied?

---

## Question 65
### Cannot access file because of mount options

Users report that files stored on a mounted filesystem cannot be executed or modified despite having the correct ownership and permission settings. The issue affects every file on the mounted storage and only began after the filesystem was mounted on a new server. Administrators suspect that the problem is related to the mount configuration rather than the files themselves. How would you investigate and resolve the issue?

---

# 4. Service & Systemd Issues

## Question 66
### Service not starting after system upgrade

A routine operating system upgrade completed successfully, but several production services now fail to start. The applications worked correctly before the upgrade, and no configuration changes were intentionally made. Business users are unable to access critical services until the issue is resolved. How would you investigate the startup failures and restore normal operation?

---

## Question 67
### Systemd service is masked

An administrator attempts to start a service, but systemd reports that the unit is masked and cannot be started. The service is required immediately to restore production functionality, yet repeated start attempts continue to fail with the same message. The reason for the service being masked is unknown. How would you determine why the service is masked and safely restore it?

---

## Question 68
### Systemd service failing because of EnvironmentFile

A production application depends on environment variables loaded through an external configuration file. Following a deployment, the service immediately fails during startup, even though the application binary itself appears to be intact. Initial investigation suggests that the problem is related to the external environment configuration. How would you determine whether the EnvironmentFile is responsible and restore the service?

---

## Question 69
### Systemd service stopping unexpectedly

A long-running production service starts successfully but unexpectedly terminates after operating normally for some time. Users experience intermittent outages because the application repeatedly stops without warning. The service logs provide only limited information regarding the shutdown. How would you investigate the unexpected termination and prevent future occurrences?

---

## Question 70
### Systemd socket activation not working

A service configured to start automatically when a client connects is no longer activating as expected. Incoming client requests fail because the application never starts, even though the associated socket unit appears to be enabled. The issue affects all users attempting to access the service. How would you investigate why socket activation is failing?

---

## Question 71
### Systemd timer not executing

A scheduled maintenance task managed through a systemd timer has stopped running automatically. The corresponding service executes successfully when started manually, but it never launches at the expected schedule. This has resulted in missed maintenance windows and outdated application data. How would you investigate why the timer is not triggering?

---

## Question 72
### Systemd service using the wrong working directory

An application managed by systemd starts successfully but immediately fails because it cannot locate required configuration files and resources. Manual execution of the application from the correct directory works without issues, indicating that the problem occurs only when started as a service. Administrators suspect that the service is running from an incorrect working directory. How would you verify and correct the configuration?

---

## Question 73
### Systemd service has an incorrect PATH

A service starts successfully when executed manually from the terminal but fails when launched through systemd. Investigation shows that commands available in an interactive shell cannot be found when the application runs as a service. The application depends on external executables that are not being located correctly. How would you determine whether the PATH configuration is causing the issue?

---

## Question 74
### Systemd service writing logs to the wrong location

Administrators are unable to locate application logs because the service is writing them to an unexpected destination. Troubleshooting has become difficult since important error messages are no longer appearing in the expected logging system. The application itself continues running, but diagnosing production issues has become significantly more difficult. How would you identify the logging configuration and redirect logs appropriately?

---

## Question 75
### Systemd service not responding to reload

A production application supports configuration reloading without requiring a full restart. However, issuing a reload command has no visible effect, forcing administrators to perform complete service restarts whenever configuration changes are required. This increases downtime and operational risk. How would you determine why the reload operation is not functioning correctly?

---

## Question 76
### Systemd service starting in the wrong order

Following a server reboot, a production application consistently fails because one of its required dependencies has not finished starting. Restarting the service manually after the system has fully booted always resolves the issue. The startup sequence appears to be incorrect, resulting in unnecessary outages after every reboot. How would you investigate and correct the service dependencies?

---

## Question 77
### Systemd service exits immediately after startup

Every attempt to start a production service results in the process exiting almost immediately with a non-zero exit status. No clients can connect because the application never remains active long enough to begin serving requests. The failure occurs consistently across multiple restart attempts. How would you investigate the immediate service termination and identify the root cause?

---

## Question 78
### Systemd service consuming excessive resources

A production service is consuming significantly more CPU and memory than expected, negatively impacting other workloads on the same server. Administrators want to ensure that the application cannot monopolize system resources while still allowing it to operate normally. The solution should improve system stability without unnecessarily restricting application performance. How would you investigate the resource usage and apply appropriate limits?

---

## Question 79
### Systemd service hangs during shutdown

Administrators attempt to stop a service for scheduled maintenance, but the shutdown process never completes. The service remains in a stopping state for an extended period, delaying maintenance activities and preventing dependent services from shutting down cleanly. A forced termination may risk data loss or corruption. How would you determine why the service is hanging during shutdown and stop it safely?

---

## Question 80
### Systemd service cannot be restarted after failure

A production service previously failed unexpectedly and remains in a failed state despite multiple restart attempts. Systemd continues refusing to start the application until the failure condition is addressed. Users remain unable to access the service, increasing production downtime. How would you investigate the failed state and restore the service to normal operation?

---


# 5. Memory & Performance Issues

## Question 81
### System is out of memory and OOM Killer is terminating processes

A production server suddenly becomes unstable as multiple applications stop responding or terminate unexpectedly. System logs indicate that the Linux Out Of Memory (OOM) Killer has started killing processes to free memory. Critical business services are affected, resulting in user downtime and failed transactions. How would you investigate the memory exhaustion and restore system stability?

---

## Question 82
### High memory usage but no process appears responsible

Monitoring tools show that nearly all physical memory is being consumed, yet no individual process appears to be using an unusually large amount of RAM. Applications have started slowing down, and administrators are unable to determine where the memory is being used. The discrepancy makes troubleshooting difficult and increases the risk of service interruption. How would you identify what is consuming memory and resolve the issue?

---

## Question 83
### Excessive swap usage

Users report that applications have become significantly slower despite the server having sufficient CPU resources. Investigation reveals that swap utilization has grown unexpectedly high, causing increased disk activity and poor response times. The server remains operational, but performance continues to deteriorate under load. How would you determine why swap usage is so high and restore acceptable performance?

---

## Question 84
### High CPU usage with no obvious process

The server consistently reports very high CPU utilization, but standard process monitoring tools do not show any application consuming excessive CPU time. Performance continues to degrade, affecting multiple production services. Administrators suspect that the workload is not being correctly reflected in the process list. How would you investigate the hidden source of CPU utilization?

---

## Question 85
### System timeouts caused by high load

Users experience frequent request timeouts across multiple applications hosted on the same server. Monitoring shows that the overall system load has increased significantly, although no single resource appears to be completely exhausted. The performance degradation is affecting business-critical services during peak usage. How would you investigate the source of the high load and restore normal response times?

---

## Question 86
### File descriptor exhaustion

Several applications begin failing with errors indicating that no additional files or network connections can be opened. Existing services continue running, but new client requests fail because system resources required for opening files and sockets have been exhausted. Administrators suspect that the system has reached its file descriptor limit. How would you investigate the exhaustion and restore normal operation?

---

## Question 87
### Excessive number of processes slowing the system

A production server has become increasingly slow, and administrators notice that an unusually large number of processes are running simultaneously. Some appear to belong to legitimate applications, while others may be orphaned or repeatedly spawned by failing services. The excessive process count is affecting overall system responsiveness. How would you identify the unnecessary processes and safely reduce system load?

---

## Question 88
### Memory fragmentation preventing large allocations

An application that requires a large contiguous block of memory begins failing allocation requests despite sufficient free memory being reported by the operating system. Smaller allocations continue working normally, making the issue difficult to identify. The application cannot continue processing until sufficient contiguous memory becomes available. How would you investigate whether memory fragmentation is responsible?

---

## Question 89
### High cache pressure affecting performance

The server spends an increasing amount of time reclaiming memory from caches, resulting in slower application performance and increased latency. Although total memory usage appears reasonable, cache eviction activity has become excessive during normal workloads. Administrators suspect that memory pressure is negatively impacting application performance. How would you investigate the cache behavior and improve system performance?

---

## Question 90
### Too many threads consuming memory

A production application creates a very large number of threads during peak workload periods. Memory consumption continues increasing even though the application's overall workload remains relatively stable. Eventually, the system begins experiencing resource exhaustion and degraded performance. How would you investigate the excessive thread creation and prevent unnecessary resource consumption?

---

## Question 91
### Excessive page faults reducing performance

Users report slow application performance even though CPU and memory utilization appear to be within normal limits. Further investigation suggests that the operating system is spending excessive time handling page faults, causing applications to wait for memory operations. Performance continues degrading as workload increases. How would you determine why page faults are occurring so frequently and improve system efficiency?

---

## Question 92
### NUMA performance issues

A high-performance application running on a multi-socket server performs significantly worse than expected, even though CPU and memory resources appear sufficient. Performance varies depending on workload placement, suggesting that memory locality may be affecting execution. Administrators suspect that NUMA behavior is responsible for the inconsistent results. How would you investigate the NUMA configuration and optimize application performance?

---

# 6. Network & Connection Issues

## Question 93
### Required port is already in use

A newly deployed application fails during startup because the required network port is already occupied by another process. The existing application using the port may be legitimate or may have been left behind by a previous deployment. Until the conflict is resolved, the new service cannot accept client connections. How would you identify the process using the port and restore the application?

---

## Question 94
### Connection refused when accessing a service

Users attempting to access a production service immediately receive a "Connection Refused" error instead of reaching the application. Network connectivity to the server appears normal, but the service itself is rejecting incoming connections. The application was functioning correctly earlier in the day before suddenly becoming unavailable. How would you investigate why connections are being refused?

---

## Question 95
### Connection attempts timing out

Users are unable to connect to a production application because every connection attempt eventually times out. Unlike an immediate connection refusal, no response is received from the destination server, leaving users waiting until the request expires. Multiple clients experience the same behavior from different locations. How would you investigate the cause of the timeout and restore connectivity?

---

## Question 96
### Intermittent network disconnections

Users report that connections to a production application randomly disconnect during normal operation. Some requests complete successfully, while others fail unexpectedly, making the problem difficult to reproduce consistently. The intermittent failures have started affecting user confidence and application reliability. How would you investigate the unstable network behavior and identify the underlying cause?

---

## Question 97
### DNS resolution failures

Applications are unable to communicate with external services because hostnames can no longer be resolved into IP addresses. Direct communication using IP addresses still works correctly, indicating that the issue is limited to name resolution. Multiple applications depending on DNS are affected simultaneously. How would you investigate the DNS failure and restore normal name resolution?

---

## Question 98
### High network latency

Users report that application response times have increased significantly despite servers remaining online and operational. Monitoring indicates unusually high network latency between application components, causing delays in communication and slower user experiences. The problem becomes more noticeable during periods of increased traffic. How would you investigate the source of the latency and improve network performance?

---

## Question 99
### Large number of TIME_WAIT connections

A production server handling a large number of client requests accumulates thousands of connections in the TIME_WAIT state. Although the application continues functioning, administrators are concerned that the growing number of connections may eventually consume available resources and reduce scalability. The issue has become increasingly noticeable as application traffic has grown. How would you investigate the large number of TIME_WAIT connections and determine whether corrective action is required?

---

## Question 100
### SSL/TLS connection failures

Clients attempting to establish secure connections with a production service receive SSL/TLS handshake failures or certificate-related errors. The application itself appears to be running normally, but secure communication cannot be established, preventing users from accessing the service. The issue began after a recent certificate renewal or configuration change. How would you investigate the secure connection failure and restore encrypted communication?

