# Linux Cheat Sheet

## Table of Contents
1. [File System](#file-system)
2. [File Permissions](#file-permissions)
3. [Creating Files and Directories](#creating-files-and-directories)
4. [Navigation](#navigation)
5. [Deleting, Copying, and Moving Files](#deleting-copying-and-moving-files)
6. [Redirecting and Piping](#redirecting-and-piping)
7. [Expansion](#expansion)
8. [Finding files](#finding-files)
9. [Time stamps](#time-stamps)
10. [Commands](#commands)
11. [Other](#other) 

## File System
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

### Chmod
| Command | Description |
| --- | --- |
| `chmod u+x file` | Add execute permission for the owner |
| `chmod g-w file` | Remove write permission for the group |
| `chmod o-r file` | Remove read permission for others |
| `chmod a=r file` | Set read permission for all |
| permission values | 0 = no permission, 1 = execute, 2 = write, 4 = read |
| `chmod 755 file` | Set read, write, and execute permissions for the owner. Set read and execute permissions for the group and others. |

## File expansion examples
| Symbol | Description |
| --- | --- |
| `*` | Matches any number of characters |
| `?` | Matches any single character |
| `[ ]` | Matches any character within the brackets |
| `[A-Z]` | Matches any uppercase letter |
| `[A-E]` | Matches any uppercase letter from A to E |
| `[a-z]` | Matches any lowercase letter |
| `[a-z]*` | Matches any lowercase letter followed by anything |
| `[0-9]` | Matches any digit |
| `[^ ]` | Matches any character not within the brackets |
| `touch {1,2,3}.txt` | Creates 3 files named 1.txt, 2.txt, and 3.txt |
| `touch {a..z}.txt` | Creates 26 files named a.txt, b.txt, c.txt, ..., z.txt |
| `touch {a..z}{1..3}.txt` | Creates 78 files named a1.txt, a2.txt, a3.txt, b1.txt, b2.txt, b3.txt, ..., z1.txt, z2.txt, z3.txt |
| `touch {Monday,Tuesday,Wednesday}.txt` | Creates 3 files named Monday.txt, Tuesday.txt, and Wednesday.txt |

## Creating Files and Directories
| Command | Description |
| --- | --- |
| `touch file.txt` | Create a new file |
| `mkdir directory` | Create a new directory |
| `mkdir -p directory/subdirectory` | Create a new directory and subdirectory |

## Commands

- [`locate`](#locate)

#### `locate`
- Find files by name. Finds files in the *whole* of the file system
- Uses a datababase to find files, the files must be updated
- `updatedb` - Updates the database used by locate

## Other
- `printenv` - Print all or part of the environment

