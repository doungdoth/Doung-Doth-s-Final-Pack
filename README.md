# Doung Doth
# Networking 3 Linux
# Journal 3

# Chapters 4 & 5

* Disks and Filesystems
____________________________________________________________________________________
User Process
_____________________________________________________________________________________
			|
_____________________________________________________________________________________	
Linux Kernel		|
[System Calls] ------------------------------------------------------------ [Device Files (nodes)]
			|								|
		[Filesystem]								|
			|								|	
		[Block Device Interface and Partition Mapping-----------------------------------------]		
			|								|
		[SCSI Subsystem and Other Drivers--------------------------------------------------------]
_____________________________________________________________________________________
			|
_____________________________________________________________________________________
Storage Device

* 4.1 Partitioning Disk Devices 
The traditional table is Master Boot Record Newer standard is called the Globally Unique Identifier Partition Table. 
Partitioning Tools:
parted- text-based tool that supports both MBR and GPT.
gparted- graphical version of parted. 
fdisk- traditional text-based Linux disk partitioning tool but does not support GPT.
gdisk-version of fdisk that supports GPT not MBR
Note-Though similar, the partition table defines simple boundaries on the disk, whereas a filesystem is a much more involved data system.

* 4.1.3 Disk and Partition Geometry
Single- platter disk consists of a spinning platter on spindle, with a head attached to moving arm that can sweep across the radius of the disk and as the head spins it reads the data. The circle is called a cylinder. Platter can have more than two head for top or bottom of platter. Divide a cylinder into slices called sectors.

* 4.2 File system
kernel and user space -the file-system= a database that transform into block device into files in hierarchy
The mkfs utility can create filesystems *create an ext4 partition with # mkfs -t ext4 /dev/sdf2

note-perform after adding a new disk or repartitioning an old on. Creating a new filesystem on top of an existing filesystem will effectively destroy the old data. 
* 4.3 Mounting filesystem
mounting- process of attaching a filesystem in Unix  $ mount command and to unmount # unmount mountpoint
UUID - type of serial number with each one being different. programs like mke2fs creates a UUID identifier when initializing the filesystem data structure.

* 4.2.10
$ df command and the outputs:
Filesystem -The filesystem device 
1024-blocks-The total capacity of the filesystem in blocks of 1024 bytes 
Used-The number of occupied blocks  Available. The number of free blocks 
Capacity-The percentage of blocks in use
 Mounted on- The mount point
note- df and du output in most Linux distributions is in 1024-byte block compared to POSIX

* 4.2.11 
fsck-The tool to check a filesystem. Prints verbose status like Pass 1: checking…
note-  never use fsck on mounted filesystem because  kernel may alter the disk data, causing runtime mismatches that can crash your system and corrupt files. use only in root partition read only single user mode.
* 4.3
$ free - free command output  the current swap usage in kilobytes.
note- swap space is dangerous on  general purpose machine. If runs out of both real memory and swap space:
Linux kernel invokes the out-of-memory (OOM) killer to kill- a process in order to free up some memory


* 4.5.2 Inside filesystem
User level Representation
* [(root)]
         /		           \			
 [dir_1]			[dir_2]
/      |	\			     |        \
[file 1] [file 2] [file 3]			[file-4]	   [file-5]

$  stat -command node information
The Virtual File System (VFS) interface layer ensures system calls always return inode numbers and link counts


* 4.53 Btrfs as an example of a next-generation filesystem



* Chapter 5 How the Linux Kernel Boots.

Simplified view of the Kernel starting/ boot:
 * 1. The machine’s BIOS or boot firmware loads and runs boot loader.
 * 2. The boot loader finds the kernel image on disk, loads it into memory starts
  * 3. The kernel initializes devices and drivers.
  * 4. The kernel mounts the root filesystem. 
 * 5. The kernel starts a program called init with a process ID of 1. This point is the user space start. 
 * 6. init sets the rest of the system processes in motion. 
 * 7. At some point, init starts a process to log in, usually near the end of the boot


* 5.1 startup messeges
messages come first from the kernel,  then from processes and initialization procedures that init starts.
use command $ dmesg but be sure to pipe the output to less because there will be much more than a screen’s worth
 * 5.2 Kernel Initialization and Boot Options 
startup- Linux Kernel general order:
 * 1. CPU inspection 
 * 2. Memory inspection 
 * 3. Device bus discovery 
 * 4. Device discovery
 * 5. Auxiliary kernel subsystem setup/networking, 
 * 6. Root filesystem mount 
 * 7. User space star


 * 5.4 Boot Loader Tasks
 Linux boot loader’s core functionality: 
Selecting among multiple kernels, switch between sets of kernel parameter, allow the user to manually override and edit kernel image and names and parameters/ single user mode, provide support for booting other OS

GRUB-Grand Unified Boot Loader -near-universal standard on Linux systems 
LILO-One of the first Linux boot loaders. ELILO is a UEFI version
SYSLINUX- Can configured to run from many kinds of filesystems 
LOADLIN- Boots a kernel from MS-DOS
efilinux- UEFI boot loader serve as a model and reference for other UEFI boot loaders
coreboot (LinuxBIOS)- high-performance replacement for PC BIOS include a kernel 
Linux Kernel EFISTUB- kernel plugin loading  kernel directly from  EFI/UEFI System Partition .

 * note-GRUB has its own “kernel” and own insmod command to dynamically load GRUB modules, completely independent of the Linux kernel
# grub-mkconfig-command is a shell script that runs everything in /etc/grub.d.
# grub-install which performs most of the work of installing the GRUB files and configuration (not Ubuntu install-grub)
Note-Incorrectly installing GRUB may break  bootup sequence system. back up your MBR with dd, back up any other currently installed GRUB directory, have a emergency backup bootup plan.
