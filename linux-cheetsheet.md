# File & Directory Operations

## List

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


### Pattern Matching (Globbing)

#### File Extension Matching
- `ls *.txt` – List files ending with `.txt`.
- `ls *.[ch]` – List source files ending with `.c` or `.h`.
- `ls *{jpg,png}` – List image files ending with `jpg` or `png`.

#### Wildcard and Character Matching
- `ls file?` – List files and directories with exactly one character after "file" (e.g., `file1`, `fileA`).
- `ls [abc]*` – List files and directories starting with `a`, `b`, or `c`.

#### Pattern Negation
- `ls [!a]*` – List files and directories not starting with `a`.

#### Directory & Hidden File Filters
- `ls -d */` – List directories only (excludes files).
- `ls -d .[!.]*` – List hidden files and directories while excluding `.` and `..`.




## Change Directory

- `cd` – Change to the home directory.
- `cd ~` – Change to the home directory.
- `cd /` – Change to the system root directory.
- `cd .` – Stay in the current directory.
- `cd ..` – Move up one directory level to the parent.
- `cd ../..` – Move up two directory levels.
- `cd -` – Change to the previous directory, toggling between the last two locations.





## Make Directory

- `mkdir <dir>` – Create a single new directory in the current location.
- `mkdir <dir1> <dir2> <dir3>` – Create multiple separate directories simultaneously.
- `mkdir -p <path/to/dir>` – Create a nested directory structure, automatically building missing parent folders.
- `mkdir -p project/{src,bin,doc,tests}` – Create a parent directory containing multiple specific subdirectories.
- `mkdir -p app/{src/{models,views},config,logs}` – Create a deeply nested multi-level project architecture in one command.
- `mkdir -v <dir>` – Create a directory and print a confirmation message for the action.
- `mkdir -pv <path/to/dir>` – Create nested parent folders while displaying a status message for every directory made.







## Remove

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





## Copy

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






## Move

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




## Link

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







