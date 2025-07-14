# Linux
### What is Linux?
* Linus Torvalds developed Linux, a Unix-like, free, open-source, and kernel operating system. Mainly it is designed for systems, servers, embedded devices, mobile devices, and mainframes and is also supported on major computer platforms such as ARM, x86, and SPARC.

### Explain the basic features of the Linux OS.
Some basic features of Linux are:

* Linux is free and easily available.
* It is more secure than other operating systems because it uses security auditing and password authentication features.
* Linux has its personal software repository.
* It includes multiple languages throughout the world. Hence Linux supports different language keyboards.
* It offers CLI and GUI to use different commands and applications such as Firefox, VLC, etc.

### Name some Linux Distros
There are various Linux distros but the following are the most commonly used:

* Ubuntu
* Debian
* CentOS
* Fedora
* RedHat

### What is Linux Kernal
* The Linux kernel is the core of a Linux operating system, acting as a bridge between hardware and software. It manages system resources, handles input/output, and provides a platform for applications to run. Essentially, it's the essential program that allows your computer to function by managing hardware and software interactions. 

### Define the basic components of Linux.
Majorly there are five basic components of Linux:

* Kernel: Linux kernel is a core part of the operating system that works as a bridge between hardware and software.
* Shell: Shell is an interface between a kernel and a user.
* GUI: Offers different way to interact with the system, known as the graphical user interface (GUI).
* Application programs: It is designed to perform a bundle of tasks through a bundle of functions.
* System Utilities: It is the software functions through which users manage the system.

### What is Bootloader in Linux
* In Linux, a bootloader is a program that loads the operating system kernel into memory when the computer starts. It acts as an intermediary between the hardware and the operating system, initializing the system and allowing the user to select which OS or kernel to boot. Common Linux bootloaders include GRUB (GRand Unified Bootloader) and LILO (Linux Loader). 

###  What is Shell in Linux?
In Linux, five Shells are used:

* csh (C Shell): This shell offers job control and spell checking and is similar to C syntax.
* ksh (Korn Shell): A high-level shell for programming languages.
* ssh (Z Shell): This shell has a unique nature, such as closing comments, startup files, file name generating, and observing logout/login watching.
* bash (Bourne Again Shell): This is the default shell for Linux.
* Fish (Friendly Interactive Shell): This shell provides auto-suggestion, web-based configuration, etc.


### What is a root account?
* The root is like the user's name or system administrator account in Linux. The root account provides complete system control, which an ordinary user cannot do.

### Describe CLI and GUI in Linux.
* CLI, i.e., command line interface. It takes input as a command and runs the tasks of the system. 
The term GUI refers to the Graphical User Interface or the human-computer interface. It uses icons, images, menus, and windows, which can be manipulated through the mouse.
 

## git commands to push the changes from local (Laptop) to the remote repository (https://github.com/)
    *   Go to the local repository folder in the laptop.
    *   Open terminal from that folder and type wsl
    *   To open vscode use the below command (in smaller case)
    *   code .
    *   vscode opens here.
    *   Edit the files which you need.
    *   Save the changes in the file.
    *   git add .   --> This will add all files from current folder to staging area in the local repository
    *   git commit -m "our message here" --> Push the changes from staging area to local git repository
    *   git push    --> Genrealy we use (git push origin main), where origin is the remote reposiotry and main is local repository. During git config we already set this up, so simple git push will merger the changes in local to remote
    *   We can see the details of the git workflow in this image  
<p align="center">
    <img width="60%" src="https://business-science.github.io/shiny-production-with-aws-book/img/09_git_cli/git_commands.png">
</p>

# Linux Commands
This page contains linux shell commands and its details

## Basic Commands
### . (dot)
* dot means current directory
### ..  (double dot)
* double dot means parent directory
### man 
* manual availabe in linux
*Example*
```
man cd
```
This will show the list of options and details for cd command. Likewise use man for other commands
### uname -a 
* Operating system version
*Example*
```
priya@LAPTOP-TSTPS35I:~$ uname -a
Linux LAPTOP-TSTPS35I 5.15.167.4-microsoft-standard-WSL2 #1 SMP Tue Nov 5 00:21:55 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux
```
### whoami 
* Username (eg:ubuntu)
*Example*
```
priya@LAPTOP-TSTPS35I:~$ whoami
priya
```
### clear
* To clear the screen (ctrl+l)
### history
* It shows all the command which you works previously
### sudo
* Root user permission (super user do)
### vi (text editor)
* Command : vi [filename]
* To insert : press i or insert button
* To save and quit : esc - shift + semicolon - :wq
* To quit : esc - shift + semicolon - :q!
### nano (It is also a text editor)
* Command : nano [filename]
### pwd (parent working directory) 
* (/home/ubuntu) --> home directory
*Example*
```
priya@LAPTOP-TSTPS35I:~$ pwd
/home/priya
```
### cd (change directory)
* cd [without arguments]    : This will return you to your home directory. 
*Example*
```
priya@LAPTOP-TSTPS35I:~$ cd
priya@LAPTOP-TSTPS35I:~$
```
* cd [directory_name]       : This will move you into the specified directory. You can use either a relative path (relative to your current directory) or an absolute path (starting from the root directory, /). 
*Example*
```
priya@LAPTOP-TSTPS35I:/$ cd mnt
priya@LAPTOP-TSTPS35I:/mnt$
```
* cd ..                     : This moves you up one level in the directory hierarchy (to the parent directory). 

*Example*

```
/mnt/d/Priyas git$ cd ..
/mnt/d$
```
* cd -                      : This will take you back to the previously visited directory. 

*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/d/Priyas git/data$ cd
priya@LAPTOP-TSTPS35I:~$ cd -
/mnt/d/Priyas git/data
priya@LAPTOP-TSTPS35I:/mnt/d/Priyas git/data$
```

* cd /                      : This will take you to the root directory. 
*Example*
```
priya@LAPTOP-TSTPS35I:/$ cd mnt
priya@LAPTOP-TSTPS35I:/mnt$ ls
c  d  e  home  wsl  wslg
priya@LAPTOP-TSTPS35I:/mnt$ cd home
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports
priya@LAPTOP-TSTPS35I:/mnt/home$ cd /
priya@LAPTOP-TSTPS35I:/$

```
* cd ~                      : This will take you to your home directory, similar to cd alone. 
*Example*
```
priya@LAPTOP-TSTPS35I:/$ cd ~
priya@LAPTOP-TSTPS35I:~$
```

### mkdir (make directory)
* To create a new directory
    * mkdir [dir_name]
* mkdir -p : It is used to create a sub directory even it doesn't exists.
    * mkdir -p [dir1]/[dir2]/[dir3]
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo mkdir Datas
[sudo] password for priya:
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports  Datas
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo mkdir -p data1/data2/data3
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports  Datas  data1
priya@LAPTOP-TSTPS35I:/mnt/home$ cd data1
priya@LAPTOP-TSTPS35I:/mnt/home/data1$ ls
data2
priya@LAPTOP-TSTPS35I:/mnt/home/data1$ cd data2
priya@LAPTOP-TSTPS35I:/mnt/home/data1/data2$ ls
data3
```

### ls (list)
* To check the list of files and directory in current folder.
* ls -lstr
    * -l : long listing format(permissions,size,etc)
    * -s : shows file size in blocks(leftmost column)
    * -t : sorts by modification time(most recent files)
    * -r : reverse the sorting order
    * -s : sorts by file(largest to smallest)
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ ls -lstr
total 12
4 drwxr-xr-x 2 root root 4096 Jul  4 06:00 AutoReports
4 drwxr-xr-x 2 root root 4096 Jul 12 21:28 Datas
4 drwxr-xr-x 3 root root 4096 Jul 12 21:30 data1
```
* ls -a : shows hidden files and directory
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ ls -a
.  ..  AutoReports  Datas  data1
```

### touch 
* To create an empty file or change the timestamp of an existing file.
    * touch [file_name.txt]
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo touch file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports  Datas  data1  file.txt
```

### rm (remove)
* To remove the file or directory.
    * rm [file_name or directory_name]
    * rm *.txt  : It will remove all the .txt files.
    * rm *      : To remove all the files.
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo rm file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports  Datas  data1
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo rm -r Datas/
priya@LAPTOP-TSTPS35I:/mnt/home$ ls
AutoReports  data1
```

### cat (concatenate)
* It is used to read and display the contents of files.
    * cat [file_name]
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ vi file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file.txt
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
```

### mv (move or rename files)
* Use the mv command to move files and directories from one directory to another or to rename a file or directory.
    * mv [options] [source-file] [destination-file]
        * source_file_name = The name of the files that we want to rename or move.
        * Destination_file_name = The name of the new location or the name of the file.
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo mv file.txt file2.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file2.txt
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file.txt
cat: file.txt: No such file or directory
```

### cp (copy)
* copies the source file specified by the SourceFile parameter to the destination file specified by the TargetFile parameter.
    * cp [options] [source] [destination]
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo cp file2.txt file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file2.txt
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file.txt
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
```

### echo
* The echo command in Linux is a built-in command that allows users to display lines of text or strings that are passed as arguments
    * echo [option] [string]

* [options] = The various options available for modifying the behavior of the `echo` command
* [string] = It is the string that we want to display.
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ echo "Hello,World!"
Hello,World!
```

### >> ( it appends the data of an existing file.)
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo cat file.txt >> file2.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file2.txt
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
Hello, Good Morning
Welcome to Linux Training Course
Have a nice day!
[or]
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo echo "Hello World" >> file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file.txt
Hello World
Hello World
```
### > (operator used for overwriting files that already exist in the directory.)
*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/home$ sudo echo "Hello World" > file.txt
priya@LAPTOP-TSTPS35I:/mnt/home$ cat file.txt
Hello World
```

## Process Management (ps, top, kill, nohup)

## Project Setup – AutoReports (LINUX Course Project)

* You are a developer managing a project named AutoReports on a Linux system.
* You are currently located in your Downloads directory:
  /home/yourusername/Downloads
* This directory contains a mix of files.
### Tasks
* Create a new project folder named AutoReports in your home directory.

*Example*

```
priya@LAPTOP-TSTPS35I:/home$ sudo mkdir AutoReports
priya@LAPTOP-TSTPS35I:/home$ ls
AutoReports  priya
```
* Inside AutoReports, create the following folder structure using a single command:
    *	src/
    *	src/scripts/
    *	src/modules/
    *	output/
    *	logs/

*Example*

```
priya@LAPTOP-TSTPS35I:/home$ cd AutoReports/
priya@LAPTOP-TSTPS35I:/home/AutoReports$ sudo mkdir -p src/scripts src/modules output logs
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports$ cd src
priya@LAPTOP-TSTPS35I:/home/AutoReports/src$ ls
modules  scripts
```
* In the Downloads directory, there are three files:
    * report1.txt
    * report2.txt
    * report_final.txt
    * Move only the files that start with report and end with .txt to the AutoReports/output/ directory.

*Example*

```
priya@LAPTOP-TSTPS35I:/mnt/c/Users/LOGAPRIYA$ cd Downloads/
priya@LAPTOP-TSTPS35I:/mnt/c/Users/LOGAPRIYA/Downloads$ touch report1.txt report2.txt report_final.txt
priya@LAPTOP-TSTPS35I:/mnt/c/Users/LOGAPRIYA/Downloads$ ls

priya@LAPTOP-TSTPS35I:/home/AutoReports$ sudo mv /mnt/c/Users/LOGAPRIYA/Downloads/report*.txt ./output/
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports$ cd output
priya@LAPTOP-TSTPS35I:/home/AutoReports/output$ ls
report1.txt  report2.txt  report_final.txt
```
* Inside src/scripts, create a blank file named main.sh and make it executable.

*Example*

```
priya@LAPTOP-TSTPS35I:/home/AutoReports/src/scripts$ sudo touch main.sh
priya@LAPTOP-TSTPS35I:/home/AutoReports/src/scripts$ ls
main.sh
```
* In the logs directory:
    * Create a file named error.log.
    * Then, create a symbolic link to error.log inside the src/ directory.

*Example*

```
priya@LAPTOP-TSTPS35I:/home/AutoReports$ sudo touch ./logs/error.log
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports$ cd logs
priya@LAPTOP-TSTPS35I:/home/AutoReports/logs$ ls
error.log

priya@LAPTOP-TSTPS35I:/home/AutoReports/logs$ cd ..
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports$ cd src
priya@LAPTOP-TSTPS35I:/home/AutoReports/src$  sudo ln -s ../logs/error.log ./error_link
priya@LAPTOP-TSTPS35I:/home/AutoReports/src$ ls
error_link  modules  scripts

```
* Remove the entire modules directory only if it exists and is empty.

*Example*

```
priya@LAPTOP-TSTPS35I:/home$ ls
AutoReports  priya
priya@LAPTOP-TSTPS35I:/home$ cd AutoReports/
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports$ cd ..
priya@LAPTOP-TSTPS35I:/home$ sudo rmdir --ignore-fail-on-non-empty AutoReports/
priya@LAPTOP-TSTPS35I:/home$ ls
AutoReports  priya
priya@LAPTOP-TSTPS35I:/home$ cd AutoReports/
priya@LAPTOP-TSTPS35I:/home/AutoReports$ ls
logs  output  src
priya@LAPTOP-TSTPS35I:/home/AutoReports/src$ cd ../..
priya@LAPTOP-TSTPS35I:/home$ sudo rm -rf AutoReports
priya@LAPTOP-TSTPS35I:/home$ ls
priya

```
## Output of tree ~/AutoReports

![alt text](image.png)

## Linux File Permission & User Management Task
### Task Scenario:
You are the Linux System Administrator for a development team named AlphaDev. You need to set up a project environment where two users collaborate on specific files and directories securely.
### Task Question:
Follow the steps below and apply proper Linux permissions and user management concepts:

1.Create Users and Groups
* Create two users:
    * dev1
    * dev2
*	Create a group named alphadev
*	Add both users to the alphadev group
*Example*
```
# To create add users  
adduser dev1
adduser dev2

# To create group 
groupadd alphadev

usermod -aG alphadev dev1
usermod -aG alphadev dev2

```
2. Setup Project Directory Structure
* Create the following directory structure under 
/opt/project_alpha:
/opt/project_alpha/
├── code/
├── docs/
└── secure/
*	Inside /opt/project_alpha/code/, create:
    *	app.sh
*	Inside /opt/project_alpha/docs/, create:
    *	readme.txt
*	Inside /opt/project_alpha/secure/, create:
    *	credentials.txt
* Use touch command to create the files.
*Example*
```
# Create directory structure
sudo mkdir -p /opt/project_alpha/{code,docs,secure}

# Create files
sudo touch /opt/project_alpha/code/app.sh
sudo touch /opt/project_alpha/docs/readme.txt
sudo touch /opt/project_alpha/secure/credentials.txt

```
3. Ownership & Permissions
* Apply the following rules:
* /opt/project_alpha	root:alphadev	770	Base directory for the project
* /opt/project_alpha/code/	dev1:alphadev	770	 ;Dev1 writes code
* /opt/project_alpha/docs/	dev2:alphadev	774 ;	Dev2 edits docs; readable by all
* /opt/project_alpha/secure/	root:root	700	;Only root can access credentials
* credentials.txt	root:root	600;	Confidential file
* Use chown and chmod to apply these rules.
*Example*
```
# 1. Base project directory
sudo chown root:alphadev /opt/project_alpha
sudo chmod 770 /opt/project_alpha

# 2. code/
sudo chown dev1:alphadev /opt/project_alpha/code
sudo chmod 770 /opt/project_alpha/code
sudo chown dev1:alphadev /opt/project_alpha/code/app.sh
sudo chmod 660 /opt/project_alpha/code/app.sh

# 3. docs/
sudo chown dev2:alphadev /opt/project_alpha/docs
sudo chmod 774 /opt/project_alpha/docs
sudo chown dev2:alphadev /opt/project_alpha/docs/readme.txt
sudo chmod 664 /opt/project_alpha/docs/readme.txt

# 4. secure/
sudo chown root:root /opt/project_alpha/secure
sudo chmod 700 /opt/project_alpha/secure
sudo chown root:root /opt/project_alpha/secure/credentials.txt
sudo chmod 600 /opt/project_alpha/secure/credentials.txt

```
4. Access Testing
*	Switch to user dev1 and test:
*	Write to app.sh
*	Read readme.txt
*	Try accessing credentials.txt (should be denied)
*	Switch to user dev2 and test:
*	Write to readme.txt
*	Try editing app.sh (should be allowed if group permission is set)
### Expected Commands to Use
*	adduser, groupadd, usermod
*	mkdir, touch
*	chown, chmod
*	su - username
*	ls -l, cat, echo, rm, rmdir
*Example*
```
# To switch users 
su - dev1
su - dev2

# As Dev1
# 1. Write to app.sh
echo "echo Hello from dev1" >> /opt/project_alpha/code/app.sh

# 2. Read readme.txt
cat /opt/project_alpha/docs/readme.txt

# 3. Try accessing credentials.txt (should fail)
cat /opt/project_alpha/secure/credentials.txt

# As Dev2
# 1. Write to readme.txt
echo "Updated by dev2" >> /opt/project_alpha/docs/readme.txt

# 2. Try editing app.sh (should succeed if group has write)
echo "Edited by dev2" >> /opt/project_alpha/code/app.sh

```
Screenshots to Submit 
1.	User & group creation (id dev1, groups dev2)
![alt text](image-1.png)
2.	ls -l showing permission setup inside /opt/project_alpha
![alt text](image-2.png)
3.	File editing attempts as both users
![alt text](image-3.png)
![alt text](image-4.png)
4.	Error on accessing credentials.txt as dev1 or dev2
![alt text](image-5.png)
