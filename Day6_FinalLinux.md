#  π Finishing for Linux!
## Topics

π Script Installation

π Errors on package managers

π Help on linux

π Linux Services

π alias

π tmux

π Wget

π find

### πScript installation

π open-source, that means we can get those scripts/programs from github.

β Syntax
β git clone <link_of_the_script_from_github>
Script modules
β Scripts are made with scripting languages(programming) like

 { python,bash,go,ruby,...}

β So when we use these programming languages to do tasks their is something called modules/libraries these are needed to run the script as the
dependencies.
β Example:
1. Python: to install python modules we use -> pip install <modulename>
i. For requirements file -> pip install -r requirements.txt
2. Go: to install go modules -> go install <modulename>
3. Ruby: to install ruby modules -> gem install <modulename>
Python installation
β If pip is not found there will be an error
β It will install
β If the package is already installed: 
Errors you may encounter
β Donβt close apt while installation
β Repository errors, if this happened you can fix it using
β sudo apt edit-sources
β And moreβ¦
β For those kinds of errors what you have to do is
google/youtube { detail we will see this while we
learn Footprinting }
Example
β To solve this:
a. Find the error
b. Search it on google
If you need help on linux about commands
You can use
β man (manual)
β This will give you the whole
manual and instruction of a
tool or command.
β  man <yourcommand>
Keys: arrow keys for navigation | q for quit
Contβ¦
β Help
β Some Commands have help
option.
β  <yourcommand> -h
β  <yourcommand> -help
β  <yourcommand> - -help
Linux Processes & Services
β As we interact with Linux, we create numbered
instances of running programs called
βprocessesβ
β To get the processes:
β ps [options]
β More commands
β ps -> for process running on my shell
β ps -A -> view all running process
β ps -u username -> view users process
β PID - Process ID
Contβ¦
β To stop process
β Kill [options] [PID]
β More on kill
β kill -19 PID -> to stop the process
β kill -18 PID -> to resume the process we stopped
β kill -9 PID -> to Stop a process immediately
β β¦ there are 31 options.
Letβs test it!
You love it?
β This is a time wasting process
β For this purpose we have the tool called βtopβ installed on linux by default.
β But to make this fun we will use βhtopβ, it is colorful and more enhanced!
- top - - htop -
To kill on htop
1. Search for the process
2. Choose SGNKILL(9) and kill it!
Foreground / backgroud
β Thus far, we have run commands at the prompt and waited for them to complete. We
call this running in the βforeground.β
β Use the β&β operator, to run programs in the βbackgroundβ or press ^Z
β To get the background process back to foreground
β Fg
To stop a process going inside your shell just press ^C 
Null device
β /dev/null - Redirects output to nowhere.
β If you want to ignore output, you can send it to the null device, /dev/null. The null
device is a special file that throws away whatever is fed to it. You may hear people refer
to it as the bit bucket. If you do not want to see errors on your screen and you do not
want to save them to a file, you can redirect them to /dev/null
β On shell output there are 2 things.
β STDERR = 2
β STDOUT = 1
β To redirect the errors from a command result we do
β command 2> filename => here if you check the file you saved on it have errors only
β To redirect the error-FREE output
β command 1>filename
β So if we redirect our commands output to /dev/null we will get error free result
β command 2> /dev/null
COntβ¦ 
alias
β Used to give a name to some bunch of
commands.
β Example: if i wanted to name ls -la βrex so
any time i want to get output of ls -la i just
type rex
β alias rex=βls -laβ
Tmux - Terminal Multiplexer
β Tmux is used to classify our terminal work.
β You can install it using apt. On kali it is built-in
β Then to start it just type βtmuxβ\
β To Create config file type
β nano .tmux.conf
β Type this
β  unbind C-b
β  unbind l
β  set -g prefix C-a
β  unbind %
β  bind e split-window -h
β  bind o split-window -v
β  set -g base-index 1
β  setw -g pane-base-index 1
β Save it | exit tmux and open again
Contβ¦
β To split horizontally

β ^A then o

β To split vertically

β ^A then e

β To exit


β ^A then x or

β just type βexitβ

β To create tab

β ^A then c

β To rename the tab

β ^A then ,(comma)

β To switch tabs

β ^A then <numbers>

β TO switch partitions

β  ^A then <arrow>

π β¦ for more you can google but be aware of our super key is ^A

### Wget
β Is a tool used to download files from websites/servers
β Syntax
β wget [options] [link]
β wget https://tldp.org/LDP/intro-linux/intro-linux.pdf
find
β ON terminal if you want to search for files/folders/musics/videos, we can use find
command.
β It is very essential tool
β Syntax:
β find [search path] [options] [search word]
- More commands
- find / -name βlinuxβ
- find /home -perm 777
- find -type f | find -type d