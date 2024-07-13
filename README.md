# Shell Basics and Permissions

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25.svg)
![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)

## Table of Contents
1. [Introduction](#introduction)
2. [Shell Basics](#shell-basics)
   - [Common Commands](#common-commands)
   - [Scripting Basics](#scripting-basics)
3. [Permissions](#permissions)
   - [File Permissions](#file-permissions)
   - [Changing Permissions](#changing-permissions)
   - [Special Permissions](#special-permissions)
4. [Examples](#examples)
5. [Resources](#resources)

## Introduction

This repository covers the fundamental concepts of shell scripting and file permissions in Unix-based systems. Whether you are a beginner or looking to brush up on your skills, this guide provides a comprehensive overview of these essential topics.

## Shell Basics

### Common Commands

The shell provides a powerful interface to interact with the operating system. Here are some common commands:

- `pwd`: Print the current working directory
- `ls`: List directory contents
- `cd`: Change the current directory
- `cp`: Copy files or directories
- `mv`: Move or rename files or directories
- `rm`: Remove files or directories
- `mkdir`: Create a new directory
- `rmdir`: Remove an empty directory

### Scripting Basics

Shell scripts are files containing a sequence of commands. Here's a simple example:

```sh
#!/bin/bash
# This is a comment
echo "Hello, World!"
```

To run this script:
1. Save it to a file, e.g., `hello.sh`
2. Make it executable: `chmod +x hello.sh`
3. Execute it: `./hello.sh`

## Permissions

### File Permissions

In Unix-like systems, each file and directory has a set of permissions that determine who can read, write, or execute it. These permissions are represented by three groups:

1. Owner
2. Group
3. Others

Each group has three types of permissions:
- `r`: Read
- `w`: Write
- `x`: Execute

You can view the permissions of a file using the `ls -l` command.

### Changing Permissions

To change permissions, use the `chmod` command. Here are some examples:

- Grant execute permission to the owner:
  ```sh
  chmod u+x file
  ```
- Remove write permission from the group:
  ```sh
  chmod g-w file
  ```
- Set read and write permissions for everyone:
  ```sh
  chmod a+rw file
  ```

### Special Permissions

There are also special permissions:
- `setuid` (Set User ID)
- `setgid` (Set Group ID)
- `sticky bit`

These can be set using the `chmod` command with numeric modes, e.g., `chmod 4755 file`.

## Examples

Here are a few examples demonstrating shell basics and permissions:

- A script to back up a directory:
  ```sh
  #!/bin/bash
  src="/path/to/source"
  dest="/path/to/destination"
  tar -czf "$dest/backup.tar.gz" "$src"
  ```

- Changing file permissions:
  ```sh
  # Grant read, write, and execute permissions to the owner
  chmod u+rwx file

  # Grant read and execute permissions to the group and others
  chmod go+rx file
  ```

## Resources

- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/bash.html)
- [Linux Permissions Guide](https://linuxhandbook.com/linux-file-permissions/)
- [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/)

