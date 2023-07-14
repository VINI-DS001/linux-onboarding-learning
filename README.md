# Linux Onboarding Course

This repository is intended to store content related to learning the Linux operating system, using Ubuntu Server

## Summary

- [1. Using the CLI in a quick and practical way](1-.-using-the-cli-in-a-quick-and-practical-way)

---
## **1. Using the CLI in a quick and practical way**

**CLI (Command-Line Interface)**: The Linux CLI (Command-Line Interface) is a way to interact with the operating system through textual commands entered into a terminal. While most people are familiar with the Linux graphical user interface (GUI), the CLI offers a more direct and flexible approach to performing tasks and managing the system. 

### **1.1 Browsing the system**

**Basic CLI commands.**

pwd: shows the user's current location on the system.

ls: identifies the contents of the current directory.

ls -a: lists all contents of the current directory, including hidden files.

touch test.arq: creates the test.arq file. To create more than one file just add another name on the command line.

ls -al: displays the content in more detail

clear: clears the CLI screen

ls —help: display the arguments for the ls command on the screen

man ls: displays the manual page for the ls command

history: displays the history of commands executed by the user.

#### **1.11 File System Hierarchy**

cd: send user to home area

To change directories, use the cd command, followed by a forward slash '/' and the name of the directory.

Example: cd/etc: changes to the etc directory

Always remember when accessing a directory through the CLI, you must keep the path.

Example: cd/var, takes you to the var directory, which contains the log directory. To access it you must complement the path, so the command must be cd/var/log

1.12 - Shortcuts for navigation

cd -: return to the previous directory

cd .. : sends the user to the parent directory of a current directory. It is possible to go back more than one directory, just add '../' to the command. If you want to go back 2 directories, use the command 'cd ../../'

cd ~: another cd shortcut that sends the user to the home area. If you want to enter a directory directly from the home area, use the cd ~/dir command. Takes you to the 'dir' directory.

### **1.2 Files and directories**

#### **1.21 Creating directories with the mkdir (make directory) command**

mkdir labs: creates the labs directory. To create more than one directory just add another name on the command line.
mkdir arqs_dirs : creates another directory inside the labs directory

It is also possible to create several directories at once with mkdir.
Example: mkdir -p dir1/dir2/dir3, creates directory dir1, which contains directory dir2, which in turn contains directory dir3.

mkdir dir\ 1: command used to create directories with separate names with a space bar. In that case, it's name will be dir 1.

#### **1.22 Removing directories and files**

mdir: delete a directory.

However, before deleting a directory, you must ensure that it is empty.

rm file1: deletes the file file1, but it can also be used to delete a directory.

rm -r: deletes all files and directories within a given directory.

rm -rf: recursive command that forcibly removes directories and their contents without requesting user confirmation. Extreme caution must be exercised when using this command.

#### **1.23 Copying files with the cp command**

cp -r dir1 dir2: copy the contents of dir1 to directory dir2.

cp -r * ../dir2: Recursively copies the entire contents of the current directory to dir2.

cp -r dir1/* dir2: copy all files and directories from dir1 to directory 2

#### **1.24 Moving and renaming with mv**

mv dir1/* dir4: moves all files and directories inside directory dir1 to dir4.

mv file1 file11: renames file1 to file2.

### **1.3 File Globbing**

#### **1.31 filtering files**

ls file*: finds files that have the prefix “file”

ls file1*: displays all files that have the “file1” prefix.

ls file1?: Adding the question mark performs the search for an additional character. To search a file with more characters, add more question marks.

ls *1*: displays all files that have the number 1 between characters.

ls ???[1-5]: determines a filter range for files that have 3 characters, and the fourth character is within the range 1 to 5.

ls ???[1,5]: when using a comma, only files whose fourth character equals 1 or 5 will be displayed.