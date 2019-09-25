# Here are some Linux commands that you can use in your work or projects. This list is helpful to users who are trying to find their way around Linux.   
 
### 1. Extract contents of a compressed folder

*sudo apt install unrar*

Run this command if you get the error message shown in the image below when trying to extract files

![Parsing error](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/1.png)

### 2. Logout of the terminal and shutdown your virtual machine

*poweroff*


### 3. ls -alh & cat .gitignore | less

*cat .gitignore* 

The cat command (short for “concatenate”) lists the contents of files to the terminal window. This is faster than opening the file in an editor, and there’s no chance you can accidentally alter the file. To read the contents of your .gitignore file, type the following command while the home directory is your current working directory.

*cat .gitignore | less*

With files longer than the number of lines in your terminal window, the text will whip past too fast for you to read. You can pipe the output from cat through less to make the process more manageable. With less you can scroll forward and backward through the file using the Up and Down Arrow keys, the PgUp and PgDn keys, and the Home and End keys. Type q to quit from less or shift key+q.

![less](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/3-1.png)

*ls -alh*

List all files and folders in the current directory in human readable format

![List all files and folders](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/3-2.png)

### 4. Freeing/Cleaning up space

Command | Use
------------ | -------------
*sudo apt autoremove* | Remove installed packages that are taking up space
*sudo du -sh var/cache/apt* | View how much space is taken up by cache
*sudo apt clean* | Clean up cache space
*du -sh ~/.cache/thumbnails/* | Check space taken up by thumbnails
*rm -rf ~/.cache/thumbnails/* | Clear thumbnail space
 
### 5. Move between/Change directories

Command | Use
------------ | -------------
*cd ~* | Switch to the user directory
*cd /* | Switch to the root directory
*cd ../..* | Move up two directories. For example, move from /home/username/d1/d2/d3/ to /home/username/d1

![root](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/5-1.png)

![Move up](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/5-2.png)

### 6. Check dependencies, Search & Purge packages

Command | Use
------------ | -------------
*apt-cache showpkg docker.io* | Use the ‘showpkg‘ sub command to check the dependencies for particular software packages. Whether those dependencies packages are installed or not. For example, use the ‘showpkg‘ command along with package-name. In this example it will return dependencies for docker.io
*apt-cache search package-name | grep application-name* | Use the ‘search’ command to check certain applications bundled with a package you have installed
*apt-cache search package-name | grep application-name* | Use the ‘search’ command to check certain applications bundled with a package you have installed
*sudo apt-get purge package-name* | Use 'purge' if you want to get rid of a package and its dependencies


![show pkg](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/6-1.png)

![search](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/6-2.png)

![purge](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/6-3.png)

### 7. Update system packages

*sudo apt-get update*

![Update](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/7.png)

### 8. Upgrade software packages

*sudo apt-get upgrade*

![Upgrade](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/8.png)

### 9. Display current mount systems

*findmnt* 

This command displays the target mount point (TARGET), the source device (SOURCE), file system type (FSTYPE), and relevant mount options (OPTIONS) for each filesystem

![mount point](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/9.png)

### 10. Display Total, Free and Used memory in human readable format

*free -mhlt*
Options:
-m, show output in megabytes
-h, show human-readable output
-l, show detailed low and high memory statistics
-t, show total for RAM + swap

![free memory low high stats](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/10-2.png)

### 11. List top processes according to RAM & CPU

*ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head*

![processes](https://github.com/kipkitur/Important-Linux-Commands/blob/master/Images/11.png)

### 12. Print total free memory in MB

*free -mht | awk '/Total/{ print $4 }'*
 

