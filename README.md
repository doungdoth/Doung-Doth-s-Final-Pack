# CSCI 2461-70 Doth, Doung 2017-08-30
# Week 2: 20 Commands

# 5 commands each from /bin, /usr/bin, /sbin, /usr/sbin

* /bin:
* Sleep: sleep is delay for a specified amount of time. cause the calling thread to be suspended from execution until either the number of realtime seconds specified by the argument seconds has elapsed or a signal is delivered to the calling thread and its action is to invoke a signal-catching function or to terminate the process.
*  Usleep: usleep suspend execution for microsecond intervals. suspends execution of the calling thread for (at least) usec microseconds. The sleep may be lengthened slightly by any system activity or by the time spent processing the call or by the granularity of system timers.  
* Nice: run a program with modified scheduling priority Run Command with an adjusted  niceness,  which  affects  process scheduling.  With no Command, print the current niceness. Nicenesses range from -20 (most favorable scheduling) to 19 (least favorable).
Chattr:  changes the file attributes on a Linux file system. When a file needs to be changed in terms of it’s attributes, use the chattr command.
* Kill: send a signal to a process signal configuration Unit configuration files for services, sockets, mount points, swap devices and scopes share a subset of configuration options which define the killing procedure of processes belonging to the unit.

* /sbin:
* watchdog: a software watchdog daemon. The Linux kernel can reset the system if serious problems are detected. This can be configured via special watchdog hardware, or via a slightly less reliable software-only watchdog inside the kernel. No matter what there needs to be a daemon that tells the kernel the system is working fine. If the daemon stops doing that, the system is reset
* swapoff: enable/disable devices and files for paging and swapping. disables swapping on the specified devices and files. When the -a flag is given, swapping is disabled on all known swap devices and files (as found in /proc/swaps or /etc/fstab)
start-stop-daemon: start and stop system daemon programs is used to control the creation and termination of system-level processes. Using one of the matching options, start-stop-daemon can be configured to find existing instances of a running process.
* Poweroff: Halt, power-off or reboot the machine. If changes to configurations were recently made, a reboot may be necessary in order to have be in effect.
* runlevel: event signaling change of system runlevel. The runlevel event signals a change of system runlevel. The new system runlevel is given in the Runlevel argument, and the 
previous system runlevel in the Prelevel argument can be empty.

* /usr/bin:
* Head: copy the first part of files. The head utility shall copy its input files to the standard output, ending the output for each file at a designated point.
* Killall:  sends a signal to all processes running any of the specified commands. If no signal name is specified, SIGTERM is sent. S signals can be specified either by 
* Flock:   locks from within shell scripts or the command line. The first and second forms wrap the lock around the executing a command, in a.
* Basename: Print NAME with any leading directory components removed. If specified, also remove a trailing Suffix. Mandatory arguments to long options are mandatory for .
* telnet: The telnet command is used to communicate with another host using the telnet protocol. If telnet is invoked without the host argument, it enters command mode, indicated by its prompt), it accepts and executes the commands listed below. If it is invoked with arguments, it performs an open command with those arguments

* /usr/sbin:
* ether-wake: ether-wake is a program that generates and transmits a Wake-On-LAN also known as (WOL) "Magic Packet". It is used for restarting machines that have been soft-powered-down. It generates the standard AMD Magic Packet format, optionally with a password included. The single required parameter is a station (MAC) address or a host ID that can be translated to a MAC address by an ethers(5) database specified in
* ethtool: ethtool is used to query and control network device driver and hardware settings, particularly for wired Ethernet devices. Used for configuring hardware settings.
* Curl: curl  is a tool to transfer data from or to a server, using one of the supported protocols: (a few… HTTPS, IMAP, TELNET TFTP). The command is designed to work without user interaction. curl offers many options including: proxy support, user authentication, FTP upload, HTTP post, SSL connections, cookies, file transfer resume. 

* i2cdetect: i2cdetect  is a userspace program to scan an I2C bus for devices. It outputs a table with the list of detected devices on the specified bus. i2cbus indicates the number or name of the I2C bus to be scanned, and should correspond to one of the busses listed by i2cdetect -l. The optional parameters first and last restrict the scanning range default: from 0x03 to 0x77



Source manual Linux man pages by SysTutorials
