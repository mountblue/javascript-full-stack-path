# Command Line Interface

Computers understand the language of zeros and ones known as binary language. In the early days of computing, instructions were provided using binary language, which is difficult for all of us to read and write. Therefore, in an operating system, there is a special program called the shell. The shell accepts human-readable commands and translates them into something the kernel can read and process.

## What Is a Shell?

- The shell is a user program or it is an environment provided for user interaction.
- It is a command language interpreter that executes commands read from the standard input device such as a keyboard or from a file.
- The shell gets started when you log in or open a console (terminal).
- Quick and dirty way to execute utilities.
- The shell is not part of the system kernel but uses the system kernel to execute programs, create files, etc.
- Several shells are available for Linux including:
- BASH ( Bourne-Again SHell ) - The most common shell in Linux. It's Open Source.
- CSH (C SHell) - The C shell's syntax and usage are very similar to the C programming language.
- KSH (Korn SHell) - Created by David Korn at AT & T Bell Labs. The Korn Shell also was the base for the POSIX Shell standard specifications.
- TCSH - It is an enhanced but completely compatible version of the Berkeley UNIX C shell (CSH).

Please note that each shell does the same job, but each understands different command syntax and provides different built-in functions. Under MS-DOS, the shell name is COMMAND.COM which is also used for the same purpose, but it is by far not as powerful as our Linux Shells are!

### Shell Prompt

There are various ways to get shell access:

- **Terminal** - Linux desktop provides a GUI based login system. Once logged in you can gain access to a shell by running X Terminal (XTerm), Gnome Terminal (GTerm), or KDE Terminal (KTerm) application.
- **Connect via secure shell (SSH)** - You will get a shell prompt as soon as you log in into a remote server or workstation.
- **Use the console** - A few Linux system also provides a text-based login system. Generally, you get a shell prompt as soon as you log in to the system.

### How do I find out my current shell name?

To find all of the available shells in your system, type the following command:

```
cat /etc/shells
```
In case the */etc/shells* file has more than one shell listed under it, then it means that more than one shell is supported by your platform.

### Command Line Interface (CLI)

The shell provides an interface to Linux where you can type or enter commands using the keyboard. It is known as the command-line interface (CLI). To find out your current shell-type following command.

```
echo $SHELL
ps $$
ps -p $$
```
The following sample output indicate that I am using bash shell:

```
PID TTY          TIME CMD
13931 pts/4    00:00:00 bash
```

## Unix Philosophy

The Unix philosophy is a philosophical approach to developing software based on the experience of leading developers of the Unix operating system. The following philosophical approaches also apply to Linux operating systems.

- *Do one thing and do it well* - Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface.
- *Everything is file* - Ease of use and security is offered by treating hardware as a file.
- *Small is beautiful.*
- *Store data and configuration in flat text files* - Text file is a universal interface. Easy to create, backup, and move to another system.
- *Use shell scripts to increase leverage and portability* - Use a shell script to automate common tasks across various UNIX / Linux installations.
- *Chain programs together to complete complex task* - Use shell pipes and filters to chain small utilities that perform one task at a time.
- *Choose portability over efficiency.*
- *Keep it Simple, Stupid (KISS).*

To know more, read this [Unix philosophy
](https://en.wikipedia.org/wiki/Unix_philosophy)


### Directory Structure and File Hierarchy

If you’re coming from Windows, the Linux file system structure can seem particularly alien. The C:\ drive and drive letters are gone, replaced by a / and cryptic-sounding directories, most of which have three-letter names.

The Filesystem Hierarchy Standard (FHS) defines the structure of file systems on Linux and other UNIX-like operating systems. However, Linux file systems also contain some directories that aren’t yet defined by the standard.

### / – The Root Directory
Everything on your Linux system is located under the / directory, known as the root directory. You can think of the / directory as being similar to the C:\ directory on Windows – but this isn’t strictly true, as Linux doesn’t have drive letters. While another partition would be located at D:\ on Windows, this other partition would appear in another folder under / on Linux.

### /bin – Essential User Binaries

The /bin directory contains the essential user binaries (programs) that must be present when the system is mounted in single-user mode. Applications such as Firefox are stored in /usr/bin, while important system programs and utilities such as the bash shell are located in /bin. The /usr directory may be stored on another partition – placing these files in the /bin directory ensures the system will have these important utilities even if no other file systems are mounted. The /sbin directory is similar – it contains essential system administration binaries.

### /etc – Configuration Files
The /etc directory contains configuration files, which can generally be edited by hand in a text editor. Note that the /etc/ directory contains system-wide configuration files – user-specific configuration files are located in each user’s home directory.

### /home – Home Folders
The /home directory contains a home folder for each user. For example, if your user name is bob, you have a home folder located at /home/bob. This home folder contains the user’s data files and user-specific configuration files. Each user only has to write access to their own home folder and must obtain elevated permissions (become the root user) to modify other files on the system.

### /opt – Optional Packages
The /opt directory contains subdirectories for optional software packages. It’s commonly used by proprietary software that doesn’t obey the standard file system hierarchy – for example, a proprietary program might dump its files in /opt/application when you install it.


### /root – Root Home Directory
The /root directory is the home directory of the root user. Instead of being located at /home/root, it’s located at /root. This is distinct from /, which is the system root directory.


### /sbin – System Administration Binaries
The /sbin directory is similar to the /bin directory. It contains essential binaries that are generally intended to be run by the root user for system administration.

### /tmp – Temporary Files
Applications store temporary files in the /tmp directory. These files are generally deleted whenever your system is restarted and may be deleted at any time by utilities such as tmpwatch.

### /usr – User Binaries & Read-Only Data
The /usr directory contains applications and files used by users, as opposed to applications and files used by the system. For example, non-essential applications are located inside the /usr/bin directory instead of the /bin directory and non-essential system administration binaries are located in the /usr/sbin directory instead of the /sbin directory. Libraries for each are located inside the /usr/lib directory. The /usr directory also contains other directories – for example, architecture-independent files like graphics are located in /usr/share.

The /usr/local directory is where locally compiled applications install to by default – this prevents them from mucking up the rest of the system.

### /var – Variable Data Files
The /var directory is the writable counterpart to the /usr directory, which must be read-only in normal operation. Log files and everything else that would normally be written to /usr during normal operation are written to the /var directory. For example, you’ll find log files in /var/log.


## Command Line Basics Crash Course

Video - [https://www.youtube.com/watch?v=cBokz0LTizk](https://www.youtube.com/watch?v=cBokz0LTizk)

Given above is a quick super-fast course in using the command line. It is intended to be done rapidly in about a day, and not meant to teach you advanced shell usage.

## Practice Drill 1

- Create the following directory structure. (Create empty files where necessary)
```
hello
├── five
│   └── six
│       ├── c.txt
│       └── seven
│           └── error.log
└── one
    ├── a.txt
    ├── b.txt
    └── two
        ├── d.txt
        └── three
            ├── e.txt
            └── four
                └── access.log
```
- Delete all the files having the `.log` extension
- Add the following content to `a.txt`
```
Unix is a family of multitasking, multiuser computer operating systems that derive from the original AT&T Unix, development starting in the 1970s at the Bell Labs research center by Ken Thompson, Dennis Ritchie, and others
```
- Delete the directory named `five`
- Rename the `one` directory to `uno`
- Move `a.txt` to the `two` directory

### Submission

Copy and paste the command for each section into a text file with explanation. At the end the exercise upload this file.

## File Permissions

Overview - [https://www.youtube.com/watch?v=D-VqgvBMV7g](https://www.youtube.com/watch?v=D-VqgvBMV7g)
Binary to Decimal Conversion for File Permissions - [https://www.youtube.com/watch?v=BmVmJi5dR9c](https://www.youtube.com/watch?v=BmVmJi5dR9c)

## Pipes and Redirection

Video 1 - [https://www.youtube.com/watch?v=Bzd7XfApxLI](https://www.youtube.com/watch?v=Bzd7XfApxLI)
Video 2 - [https://www.youtube.com/watch?v=Bzd7XfApxLI](https://www.youtube.com/watch?v=Bzd7XfApxLI)

## Practice Drill 2

### Pipes

1. Download the contents of "Harry Potter and the Goblet of fire" using the command line from [here](https://raw.githubusercontent.com/bobdeng/owlreader/master/ERead/assets/books/Harry%20Potter%20and%20the%20Goblet%20of%20Fire.txt)
2. Print the first three lines in the book
3. Print the last 10 lines in the book
4. How many times do the following words occur in the book?
    * Harry
    * Ron
    * Hermione
    * Dumbledore
5. Print lines from 100 through 200 in the book
6. How many unique words are present in the book?

___________

### Processes, ports

1. List your browser's process ids (pid) and parent process ids(ppid)
2. Stop the browser application from the command line
3. List the top 3 processes by CPU usage.
4. List the top 3 processes by memory usage.
5. Start a Python HTTP server on port 8000
6. Open another tab. Stop the process you started in the previous step
7. Start a Python HTTP server on port 90
8. Display all active connections and the corresponding TCP / UDP ports.
9. Find the pid of the process that is listening on port 5432

____________

### Managing software

Use `apt` (Ubuntu) or `homebrew` (Mac) to:


1. Install `htop`, `vim` and `nginx`
2. Uninstall `nginx`
_____________

## Misc

1. What's your local IP address?
2. Find the IP address of `google.com`
3. How to check if Internet is working using CLI?
4. Where is the `node` command located? What about `code`?

### Submission

Copy and paste the command for each section into a text file with explanation. At the end the exercise upload this file.

## How Linux Works

Go through the link here: [https://neilkakkar.com/unix.html](https://neilkakkar.com/unix.html)

Philosophy:
- Processes
- Files

Files and the File System:
- iNodes
- File Permissions
- File Linking
- File Structure

Processes:
- Attributes
- Lifecycle
- File redirection

Layers in Unix:
- The Kernel
- Unix Utilities

How the shell works:
- The Pipe
- Everything about PATHs
- Writing Shell scripts

Package Managers

Brief History of Unix

## CLI Command (for Review):

### Bread and Butter Commands - all important:
* man - Super Important
* cd ( Understand flags - dot ., double dot .., tilda~, dash -)
* mkdir
* mv
* cp with recursive flag
* ls with different flags
* pwd
* rm
* chmod - Super important
* chown - Super important
* sudo
* apt
* touch
* cat
* less
* more
* tail
* rsync
* grep
* find - Super Important
* sort
* date
* tree (needs to be installed additionally)
* wc

### OS/Process Related Commands:
* ps
* top
* df
* uname
* free
* lspci
* kill (with flags)

### Network Related Commands:
* ping
* ifconfig
* ssh

### Bash Related Commands:
* xargs
* printenv
* nano
* awk
* sed
* Pipe operator |

## Actions that you should be able to perform:

* Create/Read/Update/Delete/Move files and folders from command line
* Check disk status
* Check status of processes, able to extract process ids ( hint: use pipe operator to combine ps, xargs and awk)
* Getting the most senior parent process
* Change file permissions. Able to explain and manipulate the numerical file permissions. (chmod and chown)
* Able to extract last x lines from files, get word count for a particular word, find a particular word. (basics of sed or awk would do)
* Basics of sed and awk.
* learn what is the difference between absolute and relative paths
* Practice using absolute and relative paths
* Learn how to use the find command
* Learn ls with the 5 most commonly used flags used such as:
 -- View hidden files
 -- Sort by time
 -- Reverse sort
 -- Human readable file sizes
 -- Combining flags to get hidden files, sorted by time in reverse with human readable file sizes.
* Find out what are terminal control codes such as Ctrl + D, Ctrl + C, Ctrl + Z etc and use them
* Find out the difference between Ctrl + C and Ctrl + Z
* Find out how to use Ctrl + R to reverse search
* Find out how to use tab autocompletion
* Find out how to use the arrow keys to navigate history

## Sample Review Questions:

1. Go into your home directory
2. Create a directory d1
3. Create a file a.txt inside it
4. Check permission of a.txt. What are the permissions in decimal format?
5. What are three elements in the permission? Do you understand conversion of decimal to binary?
6. Change the permissions of a.txt to 755?
7. Add a directory d2
8. Add b.txt inside d2
9. Change permissions of d2 (and everything inside) to 755
10. Start the Firefox browser.
11. List all processes in your computer
12. Find pid of Firefox Browser. Difference between parent process and child process. (hint: you need to learn pipes)
13. Kill the process (hint: pipes, awk, xargs, kill)
14. What is your user in Linux?
15. What is your group in Linux?
16. What is your computer architecture? (hint: uname command, learn the flags)
17. What is your audio driver? (hint: lspci, learn pipes and grep)
18. Go to home folder. Use find command to find all occurrences of "java" text anywhere in any filename or directory name in your system?
19. List everything in the home directory to get all files (including hidden), sorted by time in reverse with human readable file sizes.
20. Get last x lines for Harry Potter. Get word counts for particular words.

### Questions:
1. What is the difference between service and application?
2. What are these wildcards ~, ., .., * and ??
3. What are the different flags for kill? Why do we use kill -9 in general?
4. Are you clear about file permissions? Explain them? chmod and chown commands?
5. Usage of Ctrl+R to search previously run commands, arrow keys, tab autocompletion.
