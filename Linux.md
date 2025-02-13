### 1. **General Command Flags**  
These are commonly used across multiple commands:  
- `-h` or `--help`: Display help information.  
- `-v` or `--version`: Show version information.  
- `-q` or `--quiet`: Suppress output.  
- `-y`: Assume "yes" for all prompts.  

---

### 2. **File and Directory Management (`ls`, `cp`, `mv`, `rm`)**  
- `ls`:  
  - `-l`: Long listing format.  
  - `-a`: Show all files, including hidden ones.  
  - `-h`: Human-readable file sizes.  
  - `-t`: Sort by modification time.  
  - `-r`: Reverse order.  
  - `-S`: Sort by file size.  

- `cp`:  
  - `-r`: Copy directories recursively.  
  - `-i`: Prompt before overwrite.  
  - `-u`: Copy only when the source file is newer.  
  - `-v`: Verbose mode.  

- `mv`:  
  - `-i`: Prompt before overwrite.  
  - `-u`: Move only if the source is newer.  
  - `-v`: Verbose mode.  

- `rm`:  
  - `-r`: Recursively remove directories.  
  - `-f`: Force delete without prompt.  
  - `-i`: Prompt before each removal.  

---

### 3. **File Viewing and Searching (`cat`, `less`, `grep`, `find`)**  
- `cat`:  
  - `-n`: Number all output lines.  
  - `-E`: Display `$` at the end of each line.  

- `less`:  
  - `-N`: Show line numbers.  
  - `-S`: Don't wrap long lines.  

- `grep`:  
  - `-i`: Case insensitive search.  
  - `-r`: Recursive search.  
  - `-v`: Invert match (show lines that don’t match).  
  - `-c`: Count matching lines.  
  - `-l`: List filenames with matches.  
  - `-n`: Show line numbers.  

- `find`:  
  - `-name`: Search by filename.  
  - `-type`: Filter by file type (`f` for file, `d` for directory).  
  - `-exec`: Execute a command on found files.  
  - `-size`: Search by file size.  
  - `-mtime`: Search by modification time.  

---

### 4. **System Monitoring and Process Management (`ps`, `top`, `kill`)**  
- `ps`:  
  - `-e`: Show all processes.  
  - `-f`: Full-format listing.  
  - `-u`: User-oriented format.  
  - `-p`: Show a specific process by PID.  

- `top`:  
  - `-u`: Show processes for a specific user.  
  - `-o`: Order by a specific field.  
  - `-p`: Monitor specific PIDs.  

- `kill`:  
  - `-9`: Forcefully kill a process.  
  - `-SIGTERM`: Gracefully terminate a process.  
  - `-SIGKILL`: Forcefully kill a process (same as `-9`).  

---

### 5. **Networking (`ping`, `curl`, `wget`, `netstat`, `ss`)**  
- `ping`:  
  - `-c`: Number of packets to send.  
  - `-i`: Interval between packets.  
  - `-t`: Time to live for packets.  

- `curl`:  
  - `-I`: Fetch headers only.  
  - `-O`: Save output to a file.  
  - `-d`: Send POST data.  
  - `-H`: Add custom headers.  

- `wget`:  
  - `-c`: Resume download.  
  - `-q`: Quiet mode.  
  - `-r`: Recursive download.  
  - `-p`: Download all required elements (e.g., images) for an HTML page.  

- `netstat`:  
  - `-a`: Show all connections and listening ports.  
  - `-n`: Show numerical addresses.  
  - `-t`: Show TCP connections.  
  - `-u`: Show UDP connections.  

- `ss`:  
  - `-t`: Show TCP sockets.  
  - `-u`: Show UDP sockets.  
  - `-l`: Show listening sockets.  
  - `-p`: Show process using sockets.  

---

### 6. **File Permissions and Ownership (`chmod`, `chown`)**  
- `chmod`:  
  - `-R`: Recursive permission change.  
  - `-v`: Verbose output.  

- `chown`:  
  - `-R`: Recursive ownership change.  
  - `-v`: Verbose output.  

---

### 7. **Archiving and Compression (`tar`, `gzip`, `zip`)**  
- `tar`:  
  - `-c`: Create an archive.  
  - `-x`: Extract an archive.  
  - `-v`: Verbose output.  
  - `-f`: Specify filename.  
  - `-z`: Compress with gzip.  
  - `-j`: Compress with bzip2.  

- `gzip`:  
  - `-d`: Decompress.  
  - `-v`: Verbose output.  
  - `-r`: Recursively compress.  

- `zip`:  
  - `-r`: Recursive compression.  
  - `-u`: Update files in the zip.  
  - `-d`: Delete from the zip.  

---

### 8. **User and Group Management (`useradd`, `usermod`, `passwd`, `groupadd`)**  
- `useradd`:  
  - `-m`: Create a home directory.  
  - `-s`: Specify shell.  
  - `-G`: Add to groups.  

- `usermod`:  
  - `-aG`: Add to groups without removing other group memberships.  
  - `-s`: Change shell.  
  - `-L`: Lock account.  
  - `-U`: Unlock account.  

- `passwd`:  
  - `-d`: Delete password.  
  - `-l`: Lock account.  
  - `-u`: Unlock account.  

---

### 9. **Package Management (`apt`, `yum`, `dnf`, `pacman`)**  
- `apt`:  
  - `update`: Update package lists.  
  - `upgrade`: Upgrade all packages.  
  - `install`: Install a package.  
  - `remove`: Remove a package.  

- `yum/dnf`:  
  - `install`: Install a package.  
  - `update`: Update a package.  
  - `remove`: Remove a package.  

- `pacman`:  
  - `-S`: Install packages.  
  - `-R`: Remove packages.  
  - `-U`: Upgrade packages.  
  - `-Sy`: Sync package database.
  - 
---

### 1. **Text Processing (`sed`, `awk`, `cut`, `sort`, `uniq`, `tr`)**  
- **`sed`** (Stream Editor):  
  - `-e`: Add a script to be executed.  
  - `-i`: Edit files in place.  
  - `-n`: Suppress automatic output.  
  - `-r`: Use extended regular expressions.  

- **`awk`** (Pattern Scanning and Processing):  
  - `-F`: Specify field separator.  
  - `-v`: Assign a variable.  
  - `-f`: Read awk program from a file.  

- **`cut`**:  
  - `-d`: Specify delimiter.  
  - `-f`: Select fields.  
  - `-c`: Select character positions.  

- **`sort`**:  
  - `-r`: Reverse sort order.  
  - `-n`: Numerical sort.  
  - `-k`: Specify the key (field) to sort by.  
  - `-u`: Unique sort (remove duplicates).  

- **`uniq`**:  
  - `-c`: Count occurrences.  
  - `-d`: Show only duplicates.  
  - `-u`: Show only unique lines.  

- **`tr`** (Translate/Replace):  
  - `-d`: Delete characters.  
  - `-s`: Squeeze repeated characters.  
  - `-c`: Complement the set of characters.  

---

### 2. **Permissions and ACLs (`getfacl`, `setfacl`)**  
- **`getfacl`**:  
  - `-R`: Recursively list ACLs.  
  - `-c`: Don't display the comment header.  

- **`setfacl`**:  
  - `-m`: Modify ACL.  
  - `-x`: Remove ACL.  
  - `-b`: Remove all ACLs.  
  - `-R`: Recursive operation.  

---

### 3. **System Information (`df`, `du`, `uname`, `uptime`, `who`, `dmesg`)**  
- **`df`** (Disk Free):  
  - `-h`: Human-readable sizes.  
  - `-T`: Show filesystem type.  
  - `-i`: Show inode usage.  

- **`du`** (Disk Usage):  
  - `-h`: Human-readable sizes.  
  - `-s`: Summary of total size.  
  - `-c`: Display a grand total.  
  - `-a`: Include file sizes.  

- **`uname`**:  
  - `-a`: All system information.  
  - `-r`: Kernel release.  
  - `-m`: Machine hardware name.  

- **`uptime`**:  
  - `-p`: Pretty format.  
  - `-s`: Start time of the system.  

- **`who`**:  
  - `-b`: Last system boot time.  
  - `-u`: Display idle time.  

- **`dmesg`**:  
  - `-T`: Human-readable timestamps.  
  - `-L`: Colorize output.  
  - `-l`: Filter by log level.  

---

### 4. **Disk and Filesystem Management (`mount`, `umount`, `fsck`, `mkfs`, `lsblk`, `blkid`)**  
- **`mount`**:  
  - `-a`: Mount all filesystems mentioned in fstab.  
  - `-r`: Mount as read-only.  
  - `-o`: Specify options (e.g., `rw`, `nosuid`).  

- **`umount`**:  
  - `-f`: Force unmount.  
  - `-l`: Lazy unmount (detach now, clean up later).  

- **`fsck`**:  
  - `-A`: Check all filesystems.  
  - `-r`: Interactive repair.  
  - `-y`: Automatically fix errors.  

- **`mkfs`**:  
  - `-t`: Specify filesystem type.  
  - `-c`: Check the device for bad blocks.  

- **`lsblk`**:  
  - `-f`: Show filesystem info.  
  - `-d`: Don't show children.  
  - `-o`: Custom output columns.  

- **`blkid`**:  
  - `-s`: Show specific attributes.  
  - `-c`: Specify cache file.  
  - `-p`: Probe for filesystem attributes.  

---

### 5. **Networking Advanced (`ip`, `ss`, `iptables`, `nmap`, `ssh`)**  
- **`ip`**:  
  - `addr`: Show IP addresses.  
  - `link`: Show network interfaces.  
  - `route`: Show routing table.  
  - `-s`: Display statistics.  

- **`iptables`**:  
  - `-A`: Append rule.  
  - `-D`: Delete rule.  
  - `-I`: Insert rule.  
  - `-F`: Flush all rules.  
  - `-L`: List all rules.  

- **`nmap`**:  
  - `-sP`: Ping scan.  
  - `-sS`: Stealth scan.  
  - `-O`: Detect OS.  
  - `-p`: Specify port range.  
  - `-A`: Enable OS and version detection.  

- **`ssh`**:  
  - `-i`: Identity file (private key).  
  - `-p`: Port number.  
  - `-X`: Enable X11 forwarding.  
  - `-C`: Enable compression.  

---

### 6. **Archive and Compression Advanced (`xz`, `bzip2`, `7z`)**  
- **`xz`**:  
  - `-d`: Decompress.  
  - `-k`: Keep the original file.  
  - `-v`: Verbose output.  

- **`bzip2`**:  
  - `-d`: Decompress.  
  - `-k`: Keep original file.  
  - `-v`: Verbose output.  

- **`7z`**:  
  - `a`: Add to archive.  
  - `x`: Extract files.  
  - `l`: List contents.  
  - `d`: Delete from archive.  
  - `-p`: Set password for encryption.  

---

### 7. **Development and Scripting (`make`, `gcc`, `bash`, `sed`, `awk`)**  
- **`make`**:  
  - `-f`: Specify a makefile.  
  - `-j`: Specify number of jobs (parallel).  
  - `-k`: Continue on error.  
  - `-B`: Force rebuild of all targets.  

- **`gcc`**:  
  - `-o`: Output filename.  
  - `-g`: Debugging information.  
  - `-Wall`: Show all warnings.  
  - `-O`: Optimization level.  

- **`bash`**:  
  - `-c`: Run a command.  
  - `-x`: Debug mode (show commands as executed).  
  - `-e`: Exit on error.  

---

### 8. **Other Useful Utilities**  
- **`echo`**:  
  - `-n`: No newline.  
  - `-e`: Enable interpretation of backslash escapes.  

- **`history`**:  
  - `-c`: Clear history.  
  - `-d`: Delete a specific history entry.  

- **`time`**:  
  - `-v`: Detailed resource usage.  

- **`alias` and `unalias`**:  
  - `alias`: Create shortcuts for commands.  
  - `unalias`: Remove shortcuts.  


