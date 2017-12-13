# Doung Doth
# Networking 3 Linux
# September 2, 2017

# Journal 2
# BASIC COMMANDS AND DIRECTORY HIERARCHY
 
* 2.1 boune shell /bin/sh
Shell is one of the important part of unix. Shell is a program that runs command, and servers as a small programming environment.
Shell scripts= text files that are a sequence of shell commands.
Bash or Borne again shell, is the default shell of most Linux.

* 2.23 Standard input and standard output. Unix uses I/o streams read and write data. Processes read data from input and write data to output streams. Flexible.
* 2.3 basic commands

ls= is to list the contents of a directory = -l long
cp=copies files
Mb move commands
Touch = creates a file. Doesn’t change just update if existing file
Rm- delete or remove a file
Echo = prints arguments to standard output.
Cd- is changing the current working directory + dir
Mkdir= creates a new directory dir.
Rmdir= removes the directory.
Shell globbing= shell can match simple patters to file and directory names.
* 2.5 intermediate commands

Grep- prints the lines from a file or input stream that match expression
Less- use to decrease what is shown at a time vs long list
Pwd print working directory.
Diff-see differences between wo text files
File -see a file and unsure of its format
Find and locate- =To find a certain file in a directory tree. Head and tail is a quick way to view a portion of a file and stream of data.
Sort =quickly puts the lines of text files in alphanumeric order.
CTL-D = on empty lines, stops the current standard input entry from the terminal.
CTRL-C= terminates a program regardless of input output.
Less = comand that lessens the o overview of a really big file with long output or scrolls.
* 2.6 changing password

passwd command to change password.
* 2.9 command path
path is a special environment variable . Path is  a list of system directories that the shell searches when given a command.
* 2.10 Special characters=Include Asterisk, dot, pipe forward slash etc…
* Beware to type $path corectley. If not can risk wiping out enitre path. Just start a new shell if it happens.
* 2.11 command-line editing: ctrl- (B,F,P N,A moves cursor,E,W,U,K,Y erases)
* 2.14 listing and manipulating processes:
PID=  process ID, TTY=The terminal decice where the process is running., STAT process status where memory resides. = TIME the amount of CPU time in minutes and seconds= COMMAND=can change the field.
* Every time you read, writ or execute permission is sometimes called a permission bit.
* 2.17.1 Modifying permissions
to change permissions, use chmod command. And then pick the bit to change.
chod g+r file
chmod o+r file
chmod o+r file is both combined.
Symbolic Links= is a file that points to another file or directory creating an alias like a windows shortcut.  Offfer a quick link.
Ln -s target linkname
gzip = the program (GNU zip ) one of the current standard Unix compression.
tar=o create an archive, tar cvf archive.tar file 1….
* 2.20 sudo
sudo = package allows larger distributors and admins to run commands when logged in as themselves.
su command allows to enter the root password to start root shell. No record for previous commands.
$ Sudo vipw
Use visudo command to edit/etc/sudoers, to check for file syntax errors after saved file.

# Linux Directory Hierarch Essentials
/
Bin/ 	dev/	etc/	usr/	home/	lib/	sbin/	tmp/	var/
			|					    |			
 Bin/	man/	lib/	local/	sbin/	share/			log/	tmp/



* /- Root=   Every single file and directory starts from the root directory. Only root user has write privilege under this directory.
/bin = subdirector of the root directory. Contains ready to run programs/executables. Basic unix commands include the ls and cp. Most programs in /bin are binary, created by a C compiler. Usually for booting the system
/sbin =just like /bin, /sbin also contains binary executables. Programs deal with system management, so typically by system administrator, for system maintenance purpose. ROOT is necessary when running utilities.
/usr/bin= Large directory hierarchy mostly of Linux system. contains binary files for user programs. Many names same as root directory and hold the same files for General system binaries.
/usr/sbin=Large directory hierarchy of Linux system, contains binary files for system administrators  but for Scripts with Superuser Root privileges.
/usr/local/bin=  contains users programs that you install from source

