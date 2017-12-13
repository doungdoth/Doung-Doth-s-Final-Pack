# Doung D. Doth
# CSCI 2461-70 Computer Networking 3 – Linux
# August 30, 2017
# Journal 1


# Notes from book: How Linux works

“distros” = 2 desktops = KDE and Gnome
				(UBUNTU)	
(UNITY)
Ubuntu=LXDE (used for Small or old machines) SUSE = Big distros or multiple machines
LKM= Loadable Kernal Module
What is userspace?
What is Kernal Space?

User space is the precesses that are the running programs that the kernel manages. Colectiviley make up the systems upper levels called user space aka. User Process

Kernal Process runs in Kernal- unrestricted 
User Process runs in User mode- Restricted from memory.
Kernal Space= Area kernel only access, unrestricted access to predecessor and the main Mermory.
User Mode- Restricts access to (small) subset of memory and safe cpu opoerations. Users can access

* 1.2 Hardware- understanding Main memory

Main memory- most important big storage made of 1s & 2s bits.
Cpu- instructor/operator on memory
Busy box-User interface
* 1.3 Kernal
Kernal splits memory into subdivision. Certain state
4- Systems:
PROCESSESS- kernel responsible for deteriming which process allowed use cpu
MEMORY- kernel keeps track of ALL memory: currently allocated to processes, whats shared between processes, what free space.
DEVICE DRIVERS-keral acts as interface between hardware disk and processes.
SYSTEM CALLS and Support- Processes normally use system calls to communicate with the kernel
* 1.3.1
Process management- staring, pause, resume, terminating process
Context switch- act of 1 process giving up control cpu to another
Time Slice- Each piece of TIME, allow process enough time for complex compitatioj. Kernel is responsible
* 1.3.2
MMU- Modern cpu include the Memory Management Unit, which enable a memory access scheme = Virtual Memory
Page Table- Memory address map.

* 1.3.4
System call and support
Fork () symbol – process calls fork, which enable the kernel to make identical copy processor
Exec() programs kernel stars program, replace old ones pg.7*
Pseudo devices- looks lie devices, to use process but are implemented in the software
Logs- Apps write diagonostic messages
* 1.4 User Space

User interface--------------------------------------------------------Web Browser
									Mail server			
Network configuration			Communication Bus 		Diagnostic Logging

Service T 
Complex- users on top
Utility- middle
Basic- on the bottom

Root- AKA. Super User – the most important access to all runs in the User mode NOT in Kernal

User Processes environment interaction;
Kernal – Manages Proccesses and Hardware.


# Clarity in technical reporting

As I read the article, I found some things that were a bit hard to understand and comprehend, though there were some parts to where I did understand. In summary, from what I gained from reading the article, is that one who may have an agenda, writing/essay or presentation, should have an open mind. What I mean by that is to think of yourself as the reader, the audience. Imagine they are the one who’s reading your work and are because they hope to gain something from it. Whether that’s a life changing new found information or something small like a suggestion or a tip. The information should come as interesting and engaging. The audience or reader should want to be hooked, wanting to read or hear more. Not to be reading to just read and hope stumble on some information, or to be slowly daydreaming or distracted. The whole idea is to understand both sides. 
When coming up with an idea and presenting it the many forms i.e. paper or PowerPoint, speech etc., one needs to be clear and concise. Choose words that are meaningful as if it could describe an image in one’s head. Now with the words carefully picked out, it should be in a certain language. No not a different speaking language unless it calls for it. It is the way the information is being addressed. It is having a certain tone of voice, an excitement, that one needs to have. Along with the proper grammar and formatting that one should already know, who doesn’t like pictures to go along with works? That is with the help of visual aids that can better the whole situation. It is of course must be relatable in a way that displays what you are talking about. 
These are Just some of the interesting things that I learned from reading the article, as there are many more that I left out.



