# Linux Cheat Sheet

## Table of Contents
1. [File System](#file-system)
2. [File Permissions](#file-permissions)
3. [Creating Files and Directories](#creating-files-and-directories)
4. [Navigation](#navigation)
5. [Deleting, Copying, and Moving Files](#deleting-copying-and-moving-files)
6. [Redirecting and Piping](#redirecting-and-piping)
7. [Expansion](#expansion)

## File System

### File System Hierarchy Standard (FHS)
| Directory | Description |
| --- | --- |
| `/` | Root directory |
| `/bin` | Essential command binaries. Binaries are   |
| `/boot` | Static files of the boot loader |
| `/dev` | Device files. Device files are  |
| `/etc` | Host-specific system-wide configuration files |
| `/home` | Users' home directories |
| `/lib` | Essential shared libraries and kernel modules |
| `/media` | Mount points for removable media |
| `/mnt` | Mount point for mounting a filesystem temporarily |
| `/opt` | Add-on application software packages |
| `/proc` | Virtual filesystem providing process and kernel information as files |
| `/root` | Home directory for the root user |
| `/run` | Run-time variable data |

## File Permissions
| Permission | Description |
| --- | --- |
| `r` | Read |
| `w` | Write |
| `x` | Execute |
| `s` | Set user or group ID on execution |
| `t` | Sticky bit |

### Examples of File Permissions
- `rwxr-xr--` - Owner has read, write, and execute permissions. Group has read and execute permissions. Others have only read permissions.
- `drwxr-xr-x` - Directory with read, write, and execute permissions for the owner. Read and execute permissions for the group and others.
- The first letter indicates the type of file:
  - `-` for a regular file
  - `d` for a directory
  - `l` for a symbolic link
  - `s` for a socket.
- The next 3 letters are the owner's permissions.
- The next middle 3 letters are the group's permissions.
- The last 3 letters are permissions for others.

### File expansion

| Symbol | Description |
| --- | --- |
| `*` | Matches any number of characters |
| `?` | Matches any single character |
| `[ ]` | Matches any character within the brackets |
| `[^ ]` | Matches any character not within the brackets |


## Creating Files and Directories

| Command | Description |
| --- | --- |
| `touch file.txt` | Create a new file |
| `mkdir directory` | Create a new directory |
| `mkdir -p directory/subdirectory` | Create a new directory and subdirectory |

