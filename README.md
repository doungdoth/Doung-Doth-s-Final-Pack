# Doung Doth
# Networking 3 Linux
# Journal 4

# Chapters 6 & 7

* Chapter 6
How User Space Start
kernel starts its first user-space process, init with memory and CPU
User space general starting order:
1. init 
2. Essential low-level services such as udevd and syslogd
3. Network configuration
4. Mid- and high-level services 
5. Login prompts, GUIs, high-level applications

itin- program is a user-space program along in /sbin. Starts and sttop the essential service processes on the system
three major implementations of init in Linux distributions:
System V init- A traditional sequenced init used by Linux and Red hat enterprise
system- emerging standard for init. Many distributions have moved to systemd,
Upstart-The init on Ubuntu installations, but plan to change to system

systemd is goal oriented- define a target achieve and it’s dependencies and when you want to reach the target
Upstart is reactionary- based on those events, runs jobs

*6.2 system v runlevels
$ who -r   check your system’s runlevels

*6.4 systemd

handles the regular boot process and aims to incorporate a number of standard Unix services: cron and inetd
examples nit boot- time tasks in Unix system:
Service units- Control the traditional service daemons on a Unix system
Mount units- Control the attachment of filesystems to the system. 
Target units- Control other units, usually by grouping them. The

* $ systemctl dot command
Dependency Tree
[default.target]
|
[multi-user.target]
/                               |		     \
                  [basic.target]              [cron.service]        [syslog.service]
		|
	[iptables.service]



* systemd offers a myriad of dependency basics:
Requires - Strict dependencies. systemd attempts to activate the dependency unit. If dependency unit fails, systemd deactivates the dependent unit
Wants. - Dependencies for activation only. Upon activating a unit, systemd activates the unit’s Wants dependencies, doesn’t care if those dependencies fail.
Requisite. – Units must already be active. Before requisite dependency, systemd first checks status dependency. If dependency not activated, systemd fails activation of  unit with the dependency
Conflicts. - Negative dependencies. activating a unit with conflict dependency, systemd automatically deactivates dependency if active. Simultaneous activation of two conflicting units fails.

Note= Wants dependency type is special because it does not propagate failures to other units.
* 6.4.3 systsemd configurations

$ systemctl-  view a unit’s dependencies 
# systemctl -p UnitPath show -check the current systemd configuration search path : 
$ pkg-config system-To see the system unit and configuration directories
Enabling Units
Unit files are derived from the XDG Desktop Entry Specification with section names in brackets [ ] and variable and value assignments in each section

Note=Enabling a unit is different from activating a unit. When you enable a unit, you are installing it into systemd’s configuration
-Activate a unit with systemctl start, you’re just turning it on in the current runtime environment

* 6.4.4 operations
systemctl command, which allows you to activate and deactivate services, list status, reload
activate, deactivate, and restart units, use the “systemd” start, stop, and restart commands

* 6.4.6 procss stracking and synchronization
Two fork basic startup styles:
Type=simple The service process doesn’t fork.
 Type=forking The service forks, and systemd expects the original service process to terminate. Upon termination, systemd assumes that the service is ready.

* Type startup styles indicate service itself will notify systemd when ready: 
Type=notify  -service sends a notification specific to systemd (sd_notify() function call) when is ready. 
Type=dbus -  service registers itself on the Desktop-bus/dbus when ready..




* Sequential boot timeline with a resource dependency 

Service E
[Starting][Started; Resource R ready]--------------------
Service A
	  [Starting][Started] -------------------------------
		Service B
		  [Starting][Started] -----------------------
			 Service C
			   [Starting] -----------------------



* systemctl start echo.socket- to create an activation mechanism between two units with different prefixes
$ telnet - test the service by connecting to your local port 


* 6.5.1 Upstart initialization procedure
Upstart when startup does the following:
1. Loads its configuration and the job configuration files in /etc/init. 
2. Emits the startup event.
3. Runs jobs configured to start upon receiving the startup event.
4. These initial jobs emit their own events, triggering more jobs and events.

There are two primary kinds of Upstart jobs: Task jobs and Service Jobs

$ initctl lis-You can view Upstart jobs and job status
* 6.5.3 
Stanzas
task -task stanza tells Upstart that this is a task job
expect- mountall job will spawn a daemon independently of orginal script.
stop stanza tells Upstart to terminate the job 
* 6.5.4upstar operations
 initctl start job-start upstart job
 initctl stop job -To stop a job 
 initctl restart job- To restart a job

* 6.6.4 system v init
 telinit s to switch to single-user mode
 shutdown -h now



* Chapter 7

System Configuration: Logging, System Time, Batch Jobs, and Users
sudo and su allow you to change users
/etc- system configuration files on a Linux system 

syslogd daemon- waits for messages and, depending on the type of message received, funnels the output to a file
* 7.2.2 configuring files
Linux distributions new version syslogd called rsyslogd that does more than write log messages to file
$ logger- test the system logger is to send a log message manually

* 7.3.1 /etc/passwd file
Note- logs caught by rsyslogd are not the only ones recorded by various pieces of the system

user ID (UID)-which is the user’s representation in the kernel
group ID (GID)-one of the numbered entries in the /etc/group file

* 7.3.3 The /etc/shadow File
shadow file was introduced to provide a more flexible (and more secure) way of storing passwords

passwd -changesuser’s password, but can also use -f to change the user’s real name or -s

* /etc/grou-p is a set of fields separated by colons read from left to right:
The group name-  appears when you run a command like ls -l.
The group password- hardly ever used (use sudo instead). 
 The group ID (a number)-The GID must be unique within the group file. This number goes into a user’s group field in that user’s /etc/passwd entry. 
An optional list of users that belong to the group.- users listed here, users with the corresponding group ID in their passwd file entries also belong to the group.

* 7.6.1 installing contabs files
 crontab- command installs, lists, edits, and removes a user’s crontab.
* 7.10a PAM
Pluggable Authentication Modules- easy to add support for additional authentication techniques:  two-factor and physical keys. 

easy to add support for additional authentication techniques, such as two-factor and physical keys. Authentication mechanism support, provides a limited amount of authorization control for services 


PAM flowchart steps:
pam_rootok.so -module checks to see if  root user is the one trying to authenticate
am_shells.so -module checks to see if user’s shell is in /etc/shells
pam_unix.so -module asks the user for user’s password and checks
pam_deny.so -module always fails, required control argument present, report back as chsh
