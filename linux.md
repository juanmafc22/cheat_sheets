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

## Permissions files vs directories
| Permission | File | Directory |
| --- | --- | --- |
| `r` | Read the file | Allows files in the directory to be read |
| `w` | Write to the file | Allows files in the directory to be created, deleted, or renamed |
| `x` | Execute the file | Allows the access to be directory content |

## Permission categories
| Symbol | Category |
| --- | --- |
| `u` | User |
| `g` | Group |
| `o` | Other |
| `a` | All |

## Changing permissions symbolic notation
| Symbol | Description |
| --- | --- |
| `chmod` | Change file mode bits |
| `ugoa` | Add permission to user, group, other or all |
| `+-=` | Add, subtract and set the permission |
| `rwx` | Set the permission to read, write or execute |


## Commands
- [`chmod`](#chmod)
- [`locate`](#locate)
- [`ls`](#ls) 
- [`tree`](#tree) 

### `chmod`
- Change file permission bits using symbolic notation
- `chmod u+x file` - Add execute permission for the owner
- `chmod g-w file` - Remove write permission for the group
- `chmod a=rw file` - Set read and write permissions for all
- `chmod o-r file` - Remove read permission for others
- `chmod u=rwx, g=rw, o=r file` - Set read, write, and execute permissions for the owner. Set read and write permissions for the group. Set read permissions for others
- Change the file permission using numeric notation
- `chmod 755 file` - Set read, write, and execute permissions for the owner. Set read and execute permissions for the group and others.

#### `locate`
- Find files by name. Finds files in the *whole* of the file system
- Uses a datababase to find files, the files must be updated
- `updatedb` - Updates the database used by locate

### `ls`
- List files and directories
- `ls -l` - List files in long format
- `ls -a` - List all files, including hidden files
- `ls -lh` - List files in long format with human-readable file sizes
- `ls -R` - List files recursively
- `ls -t` - List files by modification time
- `ls -tr` - List files by modification time in reverse order

### `tree`
- List files and directories in a tree-like format
- `tree -d` - List directories only
- `tree -L 2` - List files and directories up to 2 levels deep

## Other
- `printenv` - Print all or part of the environment
- `PS1` - The primary prompt string

