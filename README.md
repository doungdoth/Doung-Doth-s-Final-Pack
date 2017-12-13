# Doung Doth # 
# CSCI 2461-70 Computer Networking 3 - Linux  #
# Final Pack #
# December 13 2017 #
 
List the following: #1 Filename, #2 Purpose, #3 Expected Grade, #4 Grade Justification


# Attendance.md-
I have not been absent, and have been to each and every class meeting beginning from week 1 8/25/17, all through to the final week 12/13/17. 


The purpose of attending every class meeting is what I believe is because due to it being only a single class a week, for four hours, there is much to learn, and very little time per class meeting. I make it a a personal goal to attend each class, because I understand what is being held in class is important, whether it is regarding notes, demos, lectures,peers, assignments or just answers to potential questions, I did my best to attend each class meeting, and for the duration of the class session.
+ Expected grade: A
+ Justification: Attended every class meeting and stayed the duration of the class session.


# Journal-Week#.md
The Journals that I've completed and submitted via dropbox in d2L and are already graded are for the following weeks:
+ week 1(15/10pts) File name "linux Doung Doth Journal 1.docx"
+ week 2(10/10pts) File name "linux Doung Doth journal 2.odt" 
+ week 2 20commands(50/60pts)File name "CSCI 2461 #20 Commands.docx"
+ week 3(10/20pts)File name "linux Doung Doth Journal 3.docx"
+ week 4(10/20pts)File name "linux Doung Doth Journal 4.docx"
+ week 6(10/20pts)File name "linux Doung Doth Journal 6.docx" 


The only week journal I have missed is for week 5. 


The purpose of the Journals are to document our learnings, notes, questions/concerns and if any solutions or answers. It is also a great way to learn and retain some of the information as reading and writing goes hand in hand with one another.
+ Expected grade: C
+ Justification: Missed week 5 journal and some journals were graded 50%


# UNIX-History.md
For the UNIX history final writeup that I have completed and submitted via dropbox in d2L, was given a grade of (80/100 pts.)
+ File name "unix thread ANDROID Doung Doth journal 2-2.docx"


The purpose of the UNIX history, was to understand how the many different UNIX technological inventions created from many different companies, have begun and ended or even continue still to this day and to the future. My topic was specifically regarded to the Android softwares over the years.
+ Expected grade: B
+ Justification: Completed first draft prior to the final (200/250 pts), with final revisions and editing for the final receiving (80/100pts)


# AbantOS.md
As part of the Quality Assurance/Tester group, my contributions to AbantOS class project included: Troubleshooting/ Booting processes specifically for External Flash Drive -USB from both PC and Mac computers. Details of how to enter the Boot Manager, BIOS, enabling Legacy, and priority. My own contributions are shown below:

# What is BIOS?

* BIOS stands for Basic Input Output System referred to as BIOS. It is a software stored on a small memory chip on the motherboard. It give the computer a set of instructions on how to perform some of the basic functions such as booting and keyboard control as well as configure the hardware in a computer including the hard drive, floppy drive, USB, optical drive, CPU, and memory.

# Booting (Mac) from an external USB device

APPLE iOS MAC USER

 You can boot using an external flash drive USB using Startup Manager.

* Begin by restarting your computer by clicking the restart option with the mouse or by simply pressing the power button.

* Right when the computer begins to boot up and a sound is heard, (usually before the the logo appears) immediately press and hold the Option (⌥) key, until the Startup Manager appears.

Startup Manager will scan and list connected drives and volumes that can be booted from.

* Select the volume you want by using the mouse or arrow keys on the keyboard.

* Use the mouse to select or press the return key to select which to boot your Mac from the selected volume.

 You should now be able to boot from external flash drive USB

Another way to boot your external flash drive USB while the computer is ON, is to use what is called System Preference.

* Begin by searching and opening the the System Preferences application in the Dock.

* Click the Startup Disk pane and you will see all the disk icons available.

* Select the appropriate device or system you wish to use to boot with.

* Now restart the computer by selecting restart or by pressing the power button and then power it back on.

 You should now be able to boot the external flash drive USB.

**References**
"[How to start up Mac from bootable media](http://www.idownloadblog.com/2015/09/14/how-to-start-up-mac-from-bootable-media/)"

# Booting (PC) from an external USB device

* Begin by inserting the flash drive USB to a USB port. 

* Restart the computer (if on) by choosing to restart using the mouse, or by simply pressing the power button.

* Power on the computer back on (if off). While the computer is beginning to boot up, you will need to press the Boot Menu key to load the Boot Menu. On many computers this is the F12 key, or one of the other F row keys.

The Boot Menu should now appear. Look for anything regarding booting via USB or removable devices. 

* Use the arrow keys to highlight the desired USB or removable device and press enter to select.

The computer should now boot via flash drive USB.


If nothing happens, or it did not work, you may need to enter the BIOS to configure the settings to see the boot menu.

See USB booting issues.


# USB Booting Issues

USB Booting Issues

Did you have an issue when your PC did not boot the external flash drive USB even after going to Bios and selecting appropriate device? Did an Error message popped up saying something along the lines of "device is not found"? What do you do?

After you install what ever that it is you want on your external flash drive USB you may find out that you are finding some trouble getting it to work. This means something needs to be configured in the BIOS to allow the external flash drive USB to be recognized and booted. Once this is complete, your external hard drive USB device should now be able to run and work.

Some computers boot immediately from the internal hard drive by default, which ignores any bootable devices unless it is instructed to do otherwise. Some computers may use UEFI motherboards instead of the tradional BIOS. This all depends on the operating system, as it may support either UEFI or BIOS. 

UEFI motherboards support what is called legacy boot, which allows the computer to boot external devices instead of the internal default.

Here are the steps to to configure UEFI/Legacy Boot:

* Begin by inserting the Flash drive USB to a USB port. 

* Restart the computer by choosing to restart using the mouse, or by simply pressing the power button on the keyboard.

* While the computer is beginning to boot up, continuously press the F12 key until the Boot Menu comes up. 

If nothing happens, or it didn't work, you may need to enter the BIOS and configure the settings to see the boot menu.

* Once again, you may need to restart the computer. THIS time, instead of pressing the F12, you'll want to press the F1 Key. 
This will allow you to enter the BIOS. 

You'll want to look for anything regarding UEFI/Legacy Boot. 

* Once you find that, change the settings to enable or on. If theres and option for both, you may want to set that as well. (otherwise you'd have to change the setting back to what it was, in order to boot by default the internal hard drive (SSD)) 

* Then after you do that you'll have to change the priority. Look for anything regarding the Priority and set or enable the settings to Legacy first. This will allow the external flash drive to boot first instead of the default internal hard drive (SDD)

* Exit the menu and restart the computer either by choosing the restart options, or by powering off using the power button.

You should now be able to boot via external flash drive USB.

**References**
"[USB Troubleshooting](https://www.pcworld.com/article/3057176/hardware/the-hidden-challenges-of-booting-from-a-usb-flash-drive.html/)"


The purpose of the AbantOs class project and my contributions were to create a "User reference guide", where information was held to help assist if there were any possible questions or issues that would arise when it came to working specifically with elive-elightenment.
+ Expected grade: B
+ Justification: Participated and contributed to the best of my abilities. Whether it was in the weekly discussion board, or using GitHub and making commits/repositories. Few sections of the AbantOS, I worked on making many commits as well as other grammar edits to the whole user reference guide.

# bash_history.md


   16  sudo
   18  APUG
   20  apug
   21  ls bin
   23  ls /bin
   24  ls ~/.bash_history
   26  sudo bash
   27  exit
   29  echo
   30  sudo
   31  apt-get update
   32  apug
   33  sudo-s
   98  tar tf /dev
   99  cat
  100  apt-get
  101  apt
  102  man bash
  103  man info
  104  man help
  115  helpl
  116  help bash
  117  info bash
  155  mkdir home
  156  cd home
  157  cd eliveuser
  158  pwd
  159  ls /etc
  160  ls /home


The purpose of elive, is to experience elive as a primary OS. To experience and learn the familiarities as well as the differences when compared to other OS. elive is an free open source OS, and that meant that people world wide help contribute to the making of this. This lead to our class to use elive and to create a user reference guide that was based off our personal experience(good and bad)problems and have insightful information or solutions that would fix any trouble that others like us may encounter.
+ Expected grade: A
+ Justification: I've been using elive as my daily OS and has learned to work with elive features. There are some familiarities to iOS. I've tried out many different commands. Some included from the standard commands like ls... apug , apt-get, install ,to those my peers have come up with or found, that I found interesting from getting packages, to updating, and graphics.



