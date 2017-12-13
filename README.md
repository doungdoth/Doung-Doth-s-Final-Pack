# Doung Doth
# Networking 3 Linux
# Journal 6

# Chapters 10 & 11


# Chapter 10   Network Applications and Services
* 10.1 Basics of services
TCP- Transmission Control Protocol, a set of networking protocols that allows two or more computers to communicate, uninterrupted two-way data streams 
Note- ‘telnet’ is a program originally meant to enable logins to remote hosts but is now useful for debugging remote services
$ curl - curl utility with a special option to record details about its communication

* 10.3 Secure Shell (SSH)

SSH server- standalone most common network service applications. allows secure shell logins, remote program execution, simple file sharing. Encrypts  password and other session data, protecting you from snoopers. uses authentication  and  ciphers for session data
There are two main SSH protocol versions: 1 and 2. OpenSSH supports both, but version 1 is rarely used
OpenSSH has three host key sets: one for protocol version 1 and two for protocol 2. Each set has a public and a private key
Note= Tunneling is the process of packaging and transporting one network connection using another one
 ssh-keygen- to create a SSH protocol version 2 keys
SSH servers also use a key file called ssh_known_hosts, which contains public keys from other hosts
 chkconfig sshd on -To start sshd at boot
$ ssh remote_username@host - To log in to a remote host, run 

* use scp to transfer files to or from a remote machine to your machine one host to another:
$ scp user@host:file .
$ scp file user@host:dir
works like the command line,, using get and put commands

* 10.4 inetd and xinetd Daemons
even fields here are, from left to right:
Service name- name from /etc
Socket type. stream for TCP
Protocol-tcp or udp
Datagram server behavior-UDP wait or nowait
User-username run service
Executable-programs inetd to connect
Arguments-executables 

* 10.5

netstat- basic network service debugging tool display a number of transport and network layer statistics
options:
-t Prints TCP port information
-u Prints UDP port information
-l Prints listening ports
-a Prints every active port
-n Disables name lookups

*  lsof -I complete list of programs 

* 10.5.2. tcpodump

*  tcpdump - puts your network interface card into promiscuous mode to see whats crossing your network
Wireshark – GUI like version of tcp dump

Primitives:
tcp- TCP packets
udp- UDP packets
port port- TCP and/or UDP packets to/from port port
host host -Packets to or from host
 net network- Packets to or from network
Note- tcpdump shouldn’t snoop around on networks unless you own them.

* 10. netcat

$ netcat - netcat can connect to remote TCP/UDP ports 
$ nmap - Network Mapper program scans all ports on  machine or network of machines looking for open ports, and it lists the ports it finds

* 10.6 Remote Procedure Call (RPC)
$ rpcinf – see RPC services your computer has


* Chapter 11 Introduction to Shell Scripts

* 11.1
What are shell scripts?
shell script are a series of commands written in a file. The shell reads the commands from the file.
#!/bin/sh    -  /bin/sh program
note= run it by placing the script file in one of the directories in your command path and then running the script name on the command line.
$ chmod +rx script  - allows other users to read and execute script
$ echo- displays quote

note-using double quotes when printing large amounts of text? consider using a here document
shift-  can be used with argument variables to remove and advance

* 11.3 arguments


$# -variable holds the number of arguments passed to a script
$@- variable represents all of a script’s arguments
$$- holds the prosess id of the shell
$ ? – variable holds the exit colde of the last command shell executed
* 11.5 conditionals. 
shell has special constructs: such as:
 if/then/ else and case statements
elif -keyword that lets you string if conditionals together,

* 11.5 Fiie operations test
number of unary operations that check a file’s permissions/operators:
Tests for
-f  Regular file
-d  Directory
-h  Symbolic link
-b  Block device
-c  Character device
-p  Named pipe
-s  Socket
operator
-r  Readable
-w  Writable
-x  Executable
-u Setuid
-g Setgid
-k “Sticky”
operator               Returns true when the first argument…the second
-eq			  Equal to 
-ne 			  Not equal to 
-lt			  Less than 
-gt 			 Greater than 
-le			 Less than or equal to 
-ge			 Greater than or equal to 

* 11.6 loops
There are two types of loops in shell: for and while loops.
for loop (which is a “for each” loop) is the most common
while loop uses exit codes, like the if”conditional.

* 11.8 temporary file management
mktemp  -  command to create temporary filenames
The argument to mktemp is a template

* 11.9 here documents
<EOF tells the shell to redirect all lines that follow the standard input of the command that precedes
$ basename  - strip the extension from a filename or get rid of the directories in a full pathname

* 11.10.
awk- rarely used scripting language, is  a command prints the fifth field of the ls output
$ sed substitute some text for a regular expression
To use a subshell, put the commands to be executed by the subshell. a way to restore a part of the environment that is not permanent.
