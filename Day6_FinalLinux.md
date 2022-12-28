#  🖋 Finishing for Linux!
## Topics

📌 Script Installation

📌 Errors on package managers

📌 Help on linux

📌 Linux Services

📌 alias

📌 tmux

📌 Wget

📌 find

### 📌Script installation

🖊 open-source, that means we can get those scripts/programs from github.

● Syntax
○ git clone <link_of_the_script_from_github>
Script modules
● Scripts are made with scripting languages(programming) like

 { python,bash,go,ruby,...}

● So when we use these programming languages to do tasks their is something called modules/libraries these are needed to run the script as the
dependencies.
● Example:
1. Python: to install python modules we use -> pip install <modulename>
i. For requirements file -> pip install -r requirements.txt
2. Go: to install go modules -> go install <modulename>
3. Ruby: to install ruby modules -> gem install <modulename>
Python installation
● If pip is not found there will be an error
● It will install
● If the package is already installed: 
Errors you may encounter
● Don’t close apt while installation
● Repository errors, if this happened you can fix it using
○ sudo apt edit-sources
● And more…
➔ For those kinds of errors what you have to do is
google/youtube { detail we will see this while we
learn Footprinting }
Example
● To solve this:
a. Find the error
b. Search it on google
If you need help on linux about commands
You can use
● man (manual)
○ This will give you the whole
manual and instruction of a
tool or command.
■ man <yourcommand>
Keys: arrow keys for navigation | q for quit
Cont…
● Help
○ Some Commands have help
option.
■ <yourcommand> -h
■ <yourcommand> -help
■ <yourcommand> - -help
Linux Processes & Services
● As we interact with Linux, we create numbered
instances of running programs called
“processes”
● To get the processes:
○ ps [options]
● More commands
○ ps -> for process running on my shell
○ ps -A -> view all running process
○ ps -u username -> view users process
● PID - Process ID
Cont…
● To stop process
○ Kill [options] [PID]
● More on kill
○ kill -19 PID -> to stop the process
○ kill -18 PID -> to resume the process we stopped
○ kill -9 PID -> to Stop a process immediately
○ … there are 31 options.
Let’s test it!
You love it?
● This is a time wasting process
● For this purpose we have the tool called ‘top’ installed on linux by default.
● But to make this fun we will use ‘htop’, it is colorful and more enhanced!
- top - - htop -
To kill on htop
1. Search for the process
2. Choose SGNKILL(9) and kill it!
Foreground / backgroud
● Thus far, we have run commands at the prompt and waited for them to complete. We
call this running in the “foreground.”
● Use the “&” operator, to run programs in the “background” or press ^Z
● To get the background process back to foreground
○ Fg
To stop a process going inside your shell just press ^C 
Null device
● /dev/null - Redirects output to nowhere.
● If you want to ignore output, you can send it to the null device, /dev/null. The null
device is a special file that throws away whatever is fed to it. You may hear people refer
to it as the bit bucket. If you do not want to see errors on your screen and you do not
want to save them to a file, you can redirect them to /dev/null
● On shell output there are 2 things.
○ STDERR = 2
○ STDOUT = 1
● To redirect the errors from a command result we do
○ command 2> filename => here if you check the file you saved on it have errors only
● To redirect the error-FREE output
○ command 1>filename
● So if we redirect our commands output to /dev/null we will get error free result
○ command 2> /dev/null
COnt… 
alias
● Used to give a name to some bunch of
commands.
● Example: if i wanted to name ls -la ‘rex so
any time i want to get output of ls -la i just
type rex
○ alias rex=’ls -la’
Tmux - Terminal Multiplexer
● Tmux is used to classify our terminal work.
● You can install it using apt. On kali it is built-in
● Then to start it just type ‘tmux’\
● To Create config file type
○ nano .tmux.conf
○ Type this
■ unbind C-b
■ unbind l
■ set -g prefix C-a
■ unbind %
■ bind e split-window -h
■ bind o split-window -v
■ set -g base-index 1
■ setw -g pane-base-index 1
○ Save it | exit tmux and open again
Cont…
● To split horizontally

○ ^A then o

● To split vertically

○ ^A then e

● To exit


○ ^A then x or

○ just type ‘exit’

● To create tab

○ ^A then c

● To rename the tab

○ ^A then ,(comma)

● To switch tabs

○ ^A then <numbers>

○ TO switch partitions

■ ^A then <arrow>

🖊 … for more you can google but be aware of our super key is ^A

### Wget
● Is a tool used to download files from websites/servers
● Syntax
○ wget [options] [link]
● wget https://tldp.org/LDP/intro-linux/intro-linux.pdf
find
● ON terminal if you want to search for files/folders/musics/videos, we can use find
command.
● It is very essential tool
● Syntax:
○ find [search path] [options] [search word]
- More commands
- find / -name “linux”
- find /home -perm 777
- find -type f | find -type d