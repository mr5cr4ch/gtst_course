# βAdvanced Linux User!

# Topics
 
## π‘ Further on User management

## π‘ Linux File Ownership + Permissions

## π‘ Software Installation

## π‘ Script Installation

### πͺ To change password of user

β sudo passwd username

### πͺ To change user id

sudo passwd username

### πͺ username

sudo usermod -u new_id

### πͺ To Delete User

sudo userdel -r username

### πͺ To Change users on terminal

su - username

## π‘ note

### π‘ Sudoers file ?

β The sudoers file is a file Linux and Unix administrators use to
allocate system rights to system users.

β The user you created doesnβt have power to use sudo as the original one.

β This is Because it is not Added in the sudoers file.

Contβ¦
The 1st appearance when
you open the sudoers file
Contβ¦
You can add the User
you need to have access
to the sudoers file, so he
can use the sudo
command.
Then after the user can
use sudo command
Linux File permission
β Every file on linux
have their own
β Owner
β Permissions
β There is 5 main parts
on the listing
β Permission
β Owners
β Date
β Size
β filename
Ownership
β Ownership is the owner of
the file
β This have 2 kinds
β User
β Group
β To change the owner of file
you can use the command
β chown user:group
filename
USER GROUP
Permission
β There are 3 types of permissions
β Read ( r )
β Write ( w )
β Execute ( x )
β The folders and files are differ with
the βdβ and β-β on the beginning of
the permission.
Contβ¦
β There still the permission have three parts.
β user -group-other
β User ( u ) => power of user defined on the the
ownership
β Group (g )=> power of group defined on the
the ownership
β Other ( o ) => power of other users.
β All ( a ) => power of all which can be found in
the 3 above owners
β Command to change permission of file
β chmod <option> filename
User -group -other
CHMOD command
β This command helps to change file permission.
β Those file permissions are read,write & execute.
β Each of the permission have a number representations.
β Read -> 4 - r
β Write -> 2 - w
β Execute -> 1 - x
β Syntax
β chmod <parameter> filename
Contβ¦
β The parameter can be in numbers and symbols
A) Parameters in symbol
β chmod a+x filename -> adding execute permission for all ( chmod +x filename)
β chmod u+x filename -> adding execute permission for user
β chmod g+x filename -> adding execute permission for group
β chmod o+x filename -> adding execute permission for other
β chmod -x filename -> removing execute permission for all
β chmod a+rwx , u-rw , g-x , o-xw filename -> gives rwx for all and removes something from all
B) Parameters in Number
β chmod 621 filename -> 6 for user, 2 for group, 1 for other ( 6 = 4+2 ), 6 =r w
β chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1), 7 = rwx
+ Is giving the permission
- Is taking / removing β β
Breaktime
1. Create file called βPerm.txtβ and give the following permission to it
2. What is the equivalent of 631 permission in symbolic?
3. What is the equivalent of 200 permission in symbolic?
4. What is the numeric equivalent of
5. Create a user called gtst & test with password 123456
6. Change the file user owner of Perm.txt to gtst and the group owner to root
7. Change the user password of gtst to βpass123β
8. Change the user id of βgtstβ to 1923
9. Delete the user βtestβ
15 min
Package installation on linux
β ON linux to install softwares you use
package managers.
β Ex: apt,pacman,pkg,...
β We will use debian package manager.
β On debian the package manager i called
βAPTβ also there is called βdpkgβ
β Package managers are a free-software
user interface that work with an online
server to handle the installation and
removal of software on Debian, and
Debian-based Linux distributions.
The repository
This is the site/ server kali use to
upload the packages
Advanced package tool / apt /
β Apt is a free-software user interface that work with an
online server to handle the installation and removal of
software on Debian, and Debian-based Linux
distributions.used for online and offline purpose.
β The old βaptβ used as βapt-getβ
β Syntax
β sudo apt update
β sudo apt search <softwarename>
β sudo apt install <softwarename>
β sudo apt remove <softwarename>
β sudo apt upgrade
β sudo apt purge <softwarename>
Package dependencies
β A software can be built based on another program
called βmodulesβ
β SO, a program to work properly, the dependencies have
to be installed successfully.
β Those package managers install the
software+dependencies.
example:
Dpkg / Debian package manager /
β Dpkg is an offline package managing
program.
β Packages on debian have an extension
β.debβ
β Syntax
β sudo dpkg -i <packagename>
β sudo dpkg -r <packagename>
β sudo dpkg -P <packagename>
### πͺ my love Exresise
1. Update your system repository
2. Search for package called βcmatrixβ
3. Install βcmatrixβ
4. Remove βcmatrixβ
