# Linux
Contains Linux shell commands and details 

## git
*   go to the repository folder
*   open terminal and type wsl
*   To open vs code use this below command
*   code .
*   vs code opens here
*   edit the readme file
*   save the changes in readme file
*   git add .
*   git commit -m "our message here"
*   git push

## Basic Commands (ls, pwd, cd, mkdir, rm, touch)

### uname -a 
* Operating system version
### whoami 
* Username (eg:ubuntu)
### clear
* To clear the screen (ctrl+l)
### history
* It shows all the command which you works previously
### sudo
* Root user permission (super user do)
### vi (text editor)
* To insert : press i or insert button
* To save and quit : esc - shift + semicolon - :wq
* To quit : esc - shift + semicolon - :q!
### nano (It is also a text editor)



### pwd (parent working directory) 
* (/home/ubuntu)--> home directory

### cd (change directory)
* cd (without arguments) : This will return you to your home directory. 
* cd <directory_name> : This will move you into the specified directory. You can use either a relative path (relative to your current directory) or an absolute path (starting from the root directory, /). 
* cd .. : This moves you up one level in the directory hierarchy (to the parent directory). 

*Example*

```
/mnt/d/Priyas git$ cd ..
/mnt/d$
```
* cd - : This will take you back to the previously visited directory. 

*Example*
```
priya@LAPTOP-TSTPS35I:/mnt/d/Priyas git/data$ cd
priya@LAPTOP-TSTPS35I:~$ cd -
/mnt/d/Priyas git/data
priya@LAPTOP-TSTPS35I:/mnt/d/Priyas git/data$
```

* cd / : This will take you to the root directory. 
* cd ~ : This will take you to your home directory, similar to cd alone. 

### mkdir (make directory)
* To create a new directory
    * mkdir [dir_name]
* mkdir -p : It is used to create a sub directory even it doesn't exists.
    * mkdir -p [dir1]/[dir2]/[dir3]

### ls (list)
* To check the list of files and directory in current folder.
* ls -lstr
    * -l : long listing format(permissions,size,etc)
    * -s : shows file size in blocks(leftmost column)
    * -t : sorts by modification time(most recent files)
    * -r : reverse the sorting order
    * -s : sorts by file(largest to smallest)
* ls -a : shows hidden files and directory

### touch 
* To create an empty file or change the timestamp of an existing file.
    * touch [file_name.txt]

### rm (remove)
* To remove the file or directory.
    * rm [file_name or directory_name]
    * rm *.txt : It will remove all the .txt files.
    * rm * : To remove all the files.

### cat (concatenate)
* It is used to read and display the contents of files.
    * cat [file_name]

### mv (move or rename files)
* Use the mv command to move files and directories from one directory to another or to rename a file or directory.
    * mv [options] [source-file] [destination-file]
        * source_file_name = The name of the files that we want to rename or move.
        * Destination_file_name = The name of the new location or the name of the file.


## Project Setup – AutoReports

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