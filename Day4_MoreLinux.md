#Further on Linux
Day4_MoreLinux.md
Last time
topics
Topics
● Linux File Hierarchy
● VIM
● NANO
● Linux user management
● find command
Linux File Hierarchy
● Linux/UNIX have a special
file system than windows.
● File system is a directory
structure that the OS uses.
File system: WINDOWS 10
Cont…
● Windows: System files appear under the
local disk C:
● Linux: System files appear under the root
directory ( / )
You can Check it
in terminal also in
file manager
File structure in detail
1) / ( root )
○ Every single file and
directory starts from the
root directory
○ The only root user has the
right to write under this
directory
○ /root is the root user’s home
directory, which is not the
same as /
File structure in detail
2) bin - Binary executables
○ Essential command binaries
that need to be available in
single-user mode; for all
users
i) e.g) cat, ls, cp,pwd 
File structure in detail
3) /boot - Boot loader files
○ Kernel initrd, vmlinux, grub
files are located under /boot
○ Example:
initrd.img-2.6.32-24-generic,
vmlinuz-2.6.32-24-generic
File structure in detail
4) /dev - Essential Device files
○ These include terminal
devices, usb, or any device
attached to the system.
○ Example: /dev/tty1,
/dev/usbmon0
File structure in detail
5) /etc - et cetera
○ Contains configuration files
required by all programs.
○ This also contains startup and
shutdown shell scripts used to
start/stop individual programs.
○ Example: /etc/resolv.conf,
/etc/logrotate.conf.
File structure in detail
6) /home - Home directory
○ Home directories for all users
to store their personal files.
○ example: /home/nathan,
/home/rexder
File structure in detail
7) /lib - Libraries essential for the
binaries in /bin & /sbin
○ Library filenames are either ld*
or lib*.so.*
○ Example: ld-2.11.1.so,
libncurses.so.5.7
File structure in detail
8) /media - Mount points for
removable media such as CD-ROMs
○ Temporary mount directory
for removable devices.
○ Examples, /media/cdrom for
CD-ROM; /media/floppy for
floppy drives;
/media/cdrecorder for CD
writer
File structure in detail
9) /mnt - Temporarily mounted file
○ Temporary mount directory
where sysadmins can mount
filesystems.
File structure in detail
10) /opt - Optional application
software packages
○ Contains add-on applications
from individual vendors.
○ Add-on applications should be
installed under either /opt/ or
/opt/ sub-directory.
File structure in detail
11) /sbin - Essential system binaries
○ Just like /bin, /sbin also
contains binary executables.
○ The linux commands located
under this directory are used
typically by system
administrator, for system
maintenance purpose.
CONT… /bin
CONT… /sbin
File structure in detail
12) /tmp - Temporary Files
○ Directory that contains
temporary files created by
system and users.
○ Files under this directory are
deleted when system is
rebooted.
File structure in detail
13) /usr - User Utilities
○ - Contains binaries, libraries, documentation, and
source-code for second level programs.
○ - /usr/bin contains binary files for user programs. If
you can’t find a user binary under /bin, look under
/usr/bin. For example: at, awk, cc, less, scp
○ - /usr/sbin contains binary files for system
administrators. If you can’t find a system binary
under /sbin, look under /usr/sbin. For example: atd,
cron, sshd, useradd, userdel
○ - /usr/lib contains libraries for /usr/bin and
/usr/sbin
○ /usr/src holds the Linux kernel sources,
header-files and documentation.
Text Editors
● Programs That user for text processing.
● Linux command line text editors
○ VIM
○ Nano
○ Emacs
○ Neovim
○ ….
● Linux Graphical Text editors
○ Sublime
○ Vscode
○ Gedit
○ Pluma
○ …
VIM
● Before vi the primary editor used on Unix was the line editor
○ User was able to see/edit only one line of the text at a time
● Then then vi editor improved and developed VIM. ( VI iMproved)
● The vim editor is:
○ a very powerful
○ but at the same time it is cryptic
○ It is hard to learn, specially for windows users
● It have to modes
○ Command mode -> where you can do commands
○ Input mode -> where you can write 
Opening vim
Syntax
vim yourfilename
Vim is by default on
command mode when you
open it.
To get on insert mode you
have to type ‘i’
Insert mode
Press ‘i’
Command mode
To get back to command mode
you press ‘esc’
Cont…
● Inside Command mode you can
○ Save
○ Save & quit
○ Force Quit & Save
○ Undo
○ Execute bash commands
Save
Type
:w +
enter
Quit
Type
:q +
enter
Quit
Type
:wq! +
enter
Force = !
Undo
Type
:undo +
enter
Or :u
Execute commands
Type
:%! yourcommand
NANO
The GNU nano text editor is a user-friendly,
free and open-source text editor that
usually comes pre-installed in modern Linux
systems. 
Starting nano
Syntax
nano filename
Then start typing.
SAving Exiting & Undo_redo
Ctrl + S - save
Alt + U - Undo the ^ is equal to ‘Ctrl’
Alt + E - Redo
Ctrl + X - Exit
Paste,Copy & paste all over the linux is
Ctrl+shift+C - copy
Ctrl+shift+X - Cut
Ctrl+shift+V - Paste
You can append texts from other files with
Crtl + R and Specify the Path
Lets make our hand Dirty!
Open Your Linux
Break Time
1. Create A text file called “takeme.txt” using vim
a. Text: “ This is The Inserted Text from Planet Mars!”
b. Save and Exit
2. Create A text file called “Day3_MoreLinux.md” using
nano
a. Text: “This is day 3 course note.”
b. Save and exit
c. Open it again Read the file “takeme.txt” using nano and
add it to “Day3_MoreLinux.md”
3. Check You Notes or if you have any question about the
topics we saw write them down and Nathan Will
answer it for you
15 min
Linux User Management
● On Computer system, person who uses the computer is called “user”
● Every Users have Group.
● Users have their own file & applications.
● To know our name on linux -> “ whoami “
● Those users have power/privilege.
● On linux their is 2 kinds users.
○ Root id = 0
○ Normal User id= 1-999
The root user have the power to do everything on linux ,
but if users want to have a root access they add sudo in front of the command .
sudo YourCommand
● SUDO = Superuser do , used to pass permission denied
Creating Users
● On linux, to create users you can use the following commands
○ Useradd -> simple
○ Adduser -> Detailed
● Useradd command
○ sudo useradd username
● Adduser command
○ sudo adduser username
The User files are stored inside /etc/passwd
The User password are stored inside /etc/shadow
When you create a user it creates a group with that name.
Checking /etc/passwd
This happened what shall i do?
To access root user
Command
sudo su
