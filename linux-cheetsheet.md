# File & Directory Operations

## List (ls)

### Basic Listing
- `ls` – List files and directories in the current folder.
- `ls -a` – Show all files and directories including hidden (dot) items.
- `ls -R` – List files and directories recursively across all subdirectories.

### Long format
- `ls -l` – View long format details (permissions, owner, size, and date) for files and directories.
- `ls -lh` – View long format details with human-readable sizes (e.g., KB, MB, GB) for files and directories.
- `ls -la` – View long format details for all files and directories, including hidden items.
- `ls -laR` – View long format details for all files and directories recursively.

### Sorting
- `ls -lt` – Sort files and directories by modification time (newest at top).
- `ls -ltr` – Sort files and directories by modification time (newest at bottom).
- `ls -S` – Sort files and directories by size (largest first).
- `ls -lS` – Sort files and directories by size in long format (largest first).
- `ls -r` – Reverse the sorting order for files and directories.


### File Extension Matching
- `ls *.txt` – List files ending with `.txt`.
- `ls *.[ch]` – List source files ending with `.c` or `.h`.
- `ls *{jpg,png}` – List image files ending with `jpg` or `png`.

### Wildcard and Character Matching
- `ls file?` – List files and directories with exactly one character after "file" (e.g., `file1`, `fileA`).
- `ls [abc]*` – List files and directories starting with `a`, `b`, or `c`.

### Pattern Negation
- `ls [!a]*` – List files and directories not starting with `a`.

### Directory & Hidden File Filters
- `ls -d */` – List directories only (excludes files).
- `ls -d .[!.]*` – List hidden files and directories while excluding `.` and `..`.




## Change Directory (cd)

- `cd` – Change to the home directory.
- `cd ~` – Change to the home directory.
- `cd /` – Change to the system root directory.
- `cd .` – Stay in the current directory.
- `cd ..` – Move up one directory level to the parent.
- `cd ../..` – Move up two directory levels.
- `cd -` – Change to the previous directory, toggling between the last two locations.





## Make Directory (mkdir)

- `mkdir <dir>` – Create a single new directory in the current location.
- `mkdir <dir1> <dir2> <dir3>` – Create multiple separate directories simultaneously.
- `mkdir -p <path/to/dir>` – Create a nested directory structure, automatically building missing parent folders.
- `mkdir -p project/{src,bin,doc,tests}` – Create a parent directory containing multiple specific subdirectories.
- `mkdir -p app/{src/{models,views},config,logs}` – Create a deeply nested multi-level project architecture in one command.
- `mkdir -v <dir>` – Create a directory and print a confirmation message for the action.
- `mkdir -pv <path/to/dir>` – Create nested parent folders while displaying a status message for every directory made.




## Remove (rm)

### Basic File Removal
- `rm <file>` – Remove a single file.
- `rm <file1> <file2> <file3>` – Remove multiple files simultaneously.
- `rm *.txt` – Remove all files ending with `.txt` in the current folder.

### Directory Removal
- `rmdir <dir>` – Remove an empty directory (fails if the directory contains files).
- `rmdir <dir1> <dir2>` – Remove multiple empty directories simultaneously.
- `rm -r <dir>` – Remove a directory and all of its contents (files and subdirectories) recursively.
- `rm -r <dir1> <dir2>` – Remove multiple non-empty directories and their contents simultaneously.

### Safe and Forced Removal
- `rm -i <file>` – Prompt for confirmation before removing each file.
- `rm -ri <dir>` – Prompt for confirmation before removing each item inside a directory recursively.
- `rm -f <file>` – Force removal of files without prompting, ignoring non-existent files.
- `rm -rf <dir>` – Force recursive removal of a directory and all its contents without prompting.

### Verbose Tracking
- `rm -v <file>` – Remove a file and print a confirmation message for the action.
- `rm -rv <dir>` – Remove a directory recursively while displaying a status message for every item deleted.

### Multi-Flag Combinations
- `rm -rfv <dir>` – Force recursive removal of a directory without prompting while printing a status message for every deleted item.





## Copy(cp)

- `cp <source_file> <dest_file>` – Copy a file to a new name or location.
- `cp <file1> <file2> <file3> <dest_dir>` – Copy multiple files into a destination directory.
- `cp *.txt <dest_dir>` – Copy all files ending with `.txt` into a destination directory.
- `cp <path/to/source_file> .` – Copy a file from another location directly into the current directory.
- `cp -r <path/to/source_dir> .` – Copy a directory and its contents from another location directly into the current directory.
- `cp -r <source_dir> <dest_dir>` – Copy a directory and all of its contents (files and subdirectories) recursively.
- `cp -r <dir1> <dir2> <dest_dir>` – Copy multiple directories and their contents into a destination directory.
- `cp -i <source_file> <dest_file>` – Prompt for confirmation before overwriting an existing destination file.
- `cp -n <source_file> <dest_file>` – Do not overwrite an existing file (silently skips the copy operation).
- `cp -f <source_file> <dest_file>` – Force copying by deleting the destination file first if it cannot be opened.
- `cp -v <source_file> <dest_file>` – Copy a file and print a confirmation message showing the source and destination.
- `cp --backup <source_file> <dest_file>` – Make a backup of the destination file if it already exists before overwriting it.
- `cp -rv <source_dir> <dest_dir>` – Copy a directory recursively while displaying a status message for every item copied.
- `cp -iv <source_file> <dest_file>` – Prompt before overwriting an existing file and print a confirmation message upon a successful copy.






## Move (mv)

- `mv <old_name> <new_name>` – Rename a file or directory to a new name within the same location.
- `mv <source_file> <dest_dir>` – Move a file into a destination directory.
- `mv <file1> <file2> <file3> <dest_dir>` – Move multiple files into a destination directory simultaneously.
- `mv <source_dir> <dest_dir>` – Move a directory into a destination directory.
- `mv *.txt <dest_dir>` – Move all files ending with `.txt` into a destination directory.
- `mv <path/to/source_file> .` – Move a file from another location directly into the current directory.
- `mv <path/to/source_dir> .` – Move a directory from another location directly into the current directory.
- `mv -i <source> <dest>` – Prompt for confirmation before overwriting an existing destination file or directory.
- `mv -n <source> <dest>` – Do not overwrite an existing file or directory (silently skips the move operation).
- `mv -f <source> <dest>` – Force moving by overwriting the destination without prompting.
- `mv -v <source> <dest>` – Move an item and print a confirmation message showing the source and destination paths.
- `mv --backup <source> <dest>` – Make a backup of the destination file if it already exists before overwriting it.




## Link (ln)

### Hard Links
- `ln <target_file> <link_name>` – Create a hard link to a file (both names point directly to the same data on disk; deleting one name does not erase the actual data).
- `ln <target_file> <dest_dir>` – Create a hard link to a file inside a specific destination directory.

### Soft Links
- `ln -s <target_file> <link_name>` – Create a symbolic link shortcut to a file (deleting this shortcut leaves the source file safe; deleting the source file breaks this shortcut).
- `ln -s <target_dir> <link_name>` – Create a symbolic link shortcut to a directory.
- `ln -s <path/to/target> .` – Create a symbolic link to a file or directory directly inside the current directory.
- `ln -sv <target_file> <link_name>` – Create a symbolic link and print a confirmation message showing the link path and its target.





---

# File Viewing & Inspection


## Cat (concatenate)

- `cat <file>` – View the entire contents of a file in the terminal.
- `cat <file1> <file2>` – View the contents of multiple files concatenated sequentially.
- `cat -n <file>` – View file contents with line numbers displayed on every line.
- `cat -b <file>` – View file contents with line numbers displayed only on non-empty lines.
- `cat -s <file>` – View file contents while squeezing multiple consecutive empty lines into a single blank line.
- `cat > <file>` – Create a new file or overwrite an existing one by sending terminal input directly into it (press `Ctrl+D` to save).
- `cat >> <file>` – Append terminal input directly to the end of an existing file without overwriting it (press `Ctrl+D` to save).
- `cat <file1> <file2> > <new_file>` – Combine the contents of multiple files and overwrite them into a new destination file.
- `cat <file1> <file2> >> <existing_file>` – Append the contents of multiple files directly to the end of an existing file.
- `cat << EOF > <file>` – Create or overwrite a file with multiple lines of text from the terminal, stopping automatically when you type `EOF`.
- `cat << EOF >> <file>` – Append multiple lines of text to an existing file from the terminal, stopping automatically when you type `EOF`.






## Paged File Viewing

### less
- `less <file>` – Open a file for interactive viewing, allowing backwards and forwards scrolling without loading the entire file into memory.
- `less <file1> <file2>` – Open multiple files sequentially for viewing.
- `less +F <file>` – Open a file and automatically scroll to the bottom, continuously monitoring for new incoming data in real time (similar to `tail -f`).
- `less -N <file>` – Open a file with line numbers displayed on the left side of the screen.
- `less -S <file>` – Chop long lines horizontally instead of wrapping them to the next line (scroll left/right to read).
- `less -X <file>` – Keep the file content visible on the terminal screen after exiting the viewer.


### more
- `more <file>` – Open a file for basic forward-only viewing (press `Spacebar` to page down, `Enter` to line down, and `q` to quit).
- `more +<num> <file>` – Open a file and start displaying the contents starting exactly at line number `<num>`.




## Beginning & End of Files

### head
- `head <file>` – View the first 10 lines of a file by default.
- `head -n <num> <file>` – View the exact first `<num>` lines of a file (e.g., `head -n 20 file.txt`).
- `head -n <num> <file1> <file2>` – View the first `<num>` lines of multiple files with headers showing each file name.
- `head -n <num> -q <file1> <file2>` – View the first `<num>` lines of multiple files quietly without displaying the file name headers.

### tail
- `tail <file>` – View the last 10 lines of a file by default.
- `tail -n <num> <file>` – View the exact last `<num>` lines of a file (e.g., `tail -n 15 file.txt`).
- `tail -n +<num> <file>` – View file contents starting from line number `<num>` all the way to the end of the file.

#### Real-Time Log Monitoring
- `tail -f <file>` – View the last lines of a file and stay attached to watch new incoming data append in real time (ideal for logs).
- `tail -F <file>` – Monitor a file in real time while tracking it by name, allowing it to automatically reconnect if the log file is rotated or replaced.





## Determining File Content Type (file)

- `file <target>` – Determine the actual content type of a file or directory regardless of its file extension (e.g., ASCII text, JPEG image, ELF executable).
- `file <file1> <file2> <file3>` – Determine the content types of multiple files simultaneously.
- `file *` – Check the content type of every file and directory inside the current folder.
- `file -z <compressed_file>` – Look inside compressed files (like `.gz` or `.z`) to determine the file type of the uncompressed data hidden inside them.



---


# Permissions & Ownership


## Changing File and Directory Permissions (chmod)
- `chmod <mode> <target>` – Change the access permissions of a file or directory using numeric or symbolic notation.
- `chmod -R <mode> <dir>` – Change permissions recursively for a directory and all of its underlying files and subdirectories.
- `chmod +x <file>` – Grant execute permission to the user, group, and others simultaneously.
- `chmod u+rwx,g+rx,o-rwx <file>` – Set explicit permissions for the owner (u), group (g), and others (o) using symbolic characters.

## Changing File and Directory Ownership (chown)
- `chown <owner> <target>` – Change the owner of a file or directory to a specific user.
- `chown -R <owner> <dir>` – Change the user ownership recursively for a directory and all of its contents.
- `chown <owner>:<group> <target>` – Change both the user owner and the group ownership of a target item at the same time.
- `chown :<group> <target>` – Change only the group ownership of a target item (alternative to using `chgrp`).
- `chown --reference=<ref_file> <target>` – Copy the exact user and group ownership configuration from a reference file to a target item.

## Changing Group Ownership (chgrp)
- `chgrp <group> <target>` – Change the group ownership of a file or directory to a specific group.
- `chgrp -R <group> <dir>` – Change the group ownership recursively for a directory and all of its contents.
- `chgrp --reference=<ref_file> <target>` – Copy the exact group ownership configuration from a reference file to a target item.


## SUID (4) , SGID (2) , Sticky Bit (1)

### Set User ID (SUID)
- `chmod u+s <file>` – Set SUID on an executable file so that any user running it temporary gains the privileges of the file's owner.
- `chmod u-s <file>` – Remove SUID permission from an executable file.
- `chmod 4755 <file>` – Set SUID via octal numeric mode (adds the leading `4`) along with standard `755` permissions.

### Set Group ID (SGID)
- `chmod g+s <dir>` – Set SGID on a directory so that all new files and subdirectories created inside it automatically inherit the group ID of the parent directory.
- `chmod g+s <file>` – Set SGID on an executable file so that any user running it temporary gains the privileges of the file's group.
- `chmod g-s <target>` – Remove SGID permission from a file or directory.
- `chmod 2755 <dir>` – Set SGID via octal numeric mode (adds the leading `2`) along with standard `755` permissions.

### Sticky Bit
- `chmod +t <dir>` – Set the Sticky Bit on a shared directory (like `/tmp`) so that while any user can freely read, write, or create files inside it, they are strictly blocked from deleting, overwriting, or renaming files belonging to other users.
- `chmod -t <dir>` – Remove the Sticky Bit permission from a directory, allowing anyone with write access to delete or modify any file inside it regardless of who owns it.
- `chmod 1777 <dir>` – Set the Sticky Bit via octal numeric mode (adds the leading `1`) along with full public `777` permissions, creating a secure common folder where users can work together without risking accidental deletion of each other's data.

### Combining Special Permissions
- `chmod 6755 <target>` – Set both SUID (`4`) and SGID (`2`) permissions simultaneously via octal numeric mode (totals `6`).
- `chmod 3755 <target>` – Set both SGID (`2`) and Sticky Bit (`1`) permissions simultaneously via octal numeric mode (totals `3`).
- `chmod 7755 <target>` – Set SUID (`4`), SGID (`2`), and Sticky Bit (`1`) permissions all at once via octal numeric mode (totals `7`).






## Managing Default File Creation Permissions (umask)

- `umask` – View the current default permission mask value in octal format .
- `umask <octal_mask>` – Set a new system creation mask value using octal numbers.
  - *Example (`umask 022`):* Sets maximum directory permissions to `755` (`777 - 022`) and maximum file permissions to `644` (`666 - 022`), blocking group and public write access.
  - *Example (`umask 077`):* Sets maximum directory permissions to `700` (`777 - 077`) and maximum file permissions to `600` (`666 - 077`), making all newly created items strictly private to the owner.
- `umask u=<perms>,g=<perms>,o=<perms>` – Set the creation mask value using symbolic notation to explicitly specify allowed permissions for the owner, group, and others.
  - `umask u=rwx,g=rx,o=` – Set the creation mask value using symbolic notation to allow full access for the owner (`rwx`), read and execute access for the group (`rx`), and zero access for other users.







## Managing Access Control Lists (getfacl, setfacl)

- `getfacl <file>` – View the detailed Access Control List permissions for a file, showing specific user and group access rules beyond standard Linux permissions.
- `getfacl -R <dir>` – View the Access Control List permissions recursively for all files and subdirectories within a folder.

### Setting and Modifying Permissions
- `setfacl -m u:<user>:<perms> <file>` – Grant or modify explicit permissions (e.g., `rwx`) for a specific user on a file without changing the file's owner.
- `setfacl -m g:<group>:<perms> <file>` – Grant or modify explicit permissions for a specific group on a file.
- `setfacl -m u:<user>:<perms>,g:<group>:<perms> <file>` – Modify permissions for both a specific user and a specific group simultaneously on a single file.

### Removing Permissions
- `setfacl -x u:<user> <file>` – Remove the explicit Access Control List entry for a specific user from a file.
- `setfacl -x g:<group> <file>` – Remove the explicit Access Control List entry for a specific group from a file.
- `setfacl -b <file>` – Remove all extended Access Control List permissions from a file, reverting it entirely back to standard Linux permissions.



---



# Finding Files & Directories


## Finding Files and Directories (find)

### Basic Location and Name Matching
- `find . -name "<file_name>"` – Find files and directories inside the current folder matching an exact name.
- `find /path/to/search -iname "*<text>*"` – Find files and directories case-insensitively using wildcards anywhere in the name.
- `find . -type f` – Find files only (excludes directories from the results).
- `find . -type d` – Find directories only (excludes files from the results).

### Filtering by Size and Time
- `find . -size +100M` – Find files larger than 100 megabytes.
- `find . -size -10k` – Find files smaller than 10 kilobytes.
- `find . -mtime -7` – Find files modified within the last 7 days.
- `find . -mtime +30` – Find files modified more than 30 days ago.

### Filtering by Permissions and Ownership
- `find . -perm 755` – Find files and directories with permissions set exactly to `755`.
- `find . -user <username>` – Find files and directories owned by a specific user.




## Updating and Searching the File Database (updatedb / locate)

### Updating the Database
- `sudo updatedb` – Update the system file database immediately (requires root privileges; necessary for the `locate` command to find recently created files).

### Searching the Database
- `locate <file_name>` – Search the database to instantly find the absolute path of a file or directory anywhere on the system.
- `locate -i <file_name>` – Search the file database case-insensitively.





--- 




# Searching Text Inside Files [Global Regular Expression Print (grep)]

### Basic Text Matching
- `grep "<pattern>" <file>` – Search for a specific word or phrase inside a file and display all matching lines.
- `grep "<pattern>" <file1> <file2>` – Search for a specific text pattern across multiple files simultaneously.
- `grep -i "<pattern>" <file>` – Search for text case-insensitively, matching both uppercase and lowercase letters.
- `grep -w "<pattern>" <file>` – Search for whole words only, ignoring matches where the text is part of a larger word.

### Recursive and Location Matching
- `grep -r "<pattern>" <dir>` – Search for a text pattern recursively through all files inside a directory.
- `grep -l "<pattern>" <dir>/*` – List only the names of files that contain matching text, hiding the actual matching lines.
- `grep -L "<pattern>" <dir>/*` – List only the names of files that do not contain the matching text.

### Output Customization and Formatting
- `grep -n "<pattern>" <file>` – Display the matching lines along with their corresponding line numbers in the file.
- `grep -v "<pattern>" <file>` – Invert the search; display all lines that do not match the specified pattern.
- `grep -c "<pattern>" <file>` – Display only the total count of matching lines found inside the file instead of the lines themselves.

### Context-Based Matching
- `grep -A <num> "<pattern>" <file>` – Display the matching line plus `<num>` lines of context *after* the match.
- `grep -B <num> "<pattern>" <file>` – Display the matching line plus `<num>` lines of context *before* the match.
- `grep -C <num> "<pattern>" <file>` – Display the matching line plus `<num>` lines of context both *before and after* the match.





---




# Process Management 

### Viewing and Monitoring Processes
- `ps` – View active processes running in the current terminal session.
- `ps aux` – View detailed resource information for every active process running on the system across all users.
- `ps -ef` – View a complete list of running processes with parent process IDs (PPIDs) in full format.
- `top` – Open an interactive, real-time interface to monitor system resource usage, CPU, memory, and running processes.
- `htop` – Open an advanced, color-coded, user-friendly interactive process viewer (requires installation).

### Searching and Tracking Processes
- `pgrep <process_name>` – Search for running processes by name and return only their Process IDs (PIDs).
- `pgrep -l <process_name>` – Search for running processes by name and return both their PIDs and process names.
- `ps aux | grep <process_name>` – Search and display detailed system-wide process lines matching a specific name.
- `pidof <process_name>` – Find the exact numeric process ID of a running program by its exact name.
- `pstree` – Display running processes in a visual tree diagram to show parent-child relationships.

### Finding Resource and Port Locks
- `lsof` – List all open files on the system and the processes currently using them.
- `lsof -i :<port>` – Find the specific process currently using or blocking a network port (e.g., `lsof -i :8080`).
- `fuser <file>` – Identify the Process ID of any program currently accessing a specific file or directory.
- `fuser -k <file>` – Kill the process currently accessing a specific file or directory to free it up.

### Termination and Signals
- `kill <pid>` – Send a default `TERM` (15) signal to terminate a process gracefully using its Process ID.
- `kill -9 <pid>` – Send a `KILL` (9) signal to force-quit a process immediately, bypassing any cleanup operations.
- `kill -l` – List all available signal names and numbers that can be sent to processes.
- `killall <process_name>` – Terminate all running instances of a process simultaneously by using its name instead of its PID.
- `killall -9 <process_name>` – Force-terminate all running instances of a process simultaneously by name.
- `pkill <pattern>` – Terminate processes based on a full or partial match of their name or command line.
- `pkill -u <username>` – Terminate all active processes belonging to a specific user.

### Process Priority (Nice Levels)
- `nice -n <value> <command>` – Start a new process with a specific priority level (values range from -20 highest to 19 lowest).
- `renice -n <value> -p <pid>` – Change the priority level of an already running process while it is active.

### Background and Foreground Jobs
- `jobs` – List all active background jobs running in the current shell session.
- `<command> &` – Run a command in the background immediately, leaving the terminal free for other tasks.
- `bg %<job_id>` – Resume a paused or stopped background job, keeping it running in the background.
- `fg %<job_id>` – Bring a background job into the foreground, taking control of the active terminal session.
- `nohup <command> &` – Run a command in the background that will continue running even if you log out or close the terminal.
- `disown %<job_id>` – Remove a background job from the shell's active job table so it won't close when the shell exits.

### Finding Shell Process IDs
- `echo $$` – Display the Process ID (PID) of the currently active terminal shell session.
- `echo $PPID` – Display the Parent Process ID (PPID) of the current shell session (typically the terminal emulator or SSH daemon).
- `ps -p $$` – Display the active process details for the current shell session only.

### Finding Parent Process Details
- `ps -p $PPID` – Display process details for the parent application that launched the current shell.
- `ps -o ppid= -p <pid>` – Print only the numeric parent process ID of a specific process, removing all headers.

### Tracing System Calls and Processes (strace)
- `strace <command>` – Run a command while intercepting and displaying all system calls, arguments, and return values made to the Linux kernel (e.g., `strace ls` to trace the file system calls made when listing a directory).
- `strace -p <pid>` – Attach directly to a currently running process by its PID to trace its active system calls in real time (press `Ctrl+C` to detach).
- `strace -c <command>` – Run a command and print a summary table of all system calls made, including execution time, call counts, and errors, instead of raw lines.
- `strace -o <output_file> <command>` – Run a command and redirect the extensive system call trace log directly into a specific file.
- `strace -e <system_call> <command>` – Trace only specific system calls during execution (e.g., `strace -e openat,readls` to monitor only file opening and reading).
- `strace -f <command>` – Trace a process along with any child processes it creates or forks during execution.



















