## Useful Linux Commands

#### CPU Usage and Running Process

`top`

Press 'i' to off the idle process visibility, 'M' for sort the processes in memory usage, 'S' for running time.<br/> 

`htop`

`ps aux | grep -i anirban`

The advantage of **ps** command is one can easily find processes associated with the term *anirban*

`pidof anirban`

`pgrep anir`

The commands like *top* and *ps* help to find all the running and idle processes in your system. If you happen to know the process name (or part of a process name), you can use *pidof* (*pgrep*) command.


#### Kill a process

`kill -9 <process_id>`

You can use -9 or -SIGKILL to kill the process immediately. If you dont write any of these flags, the system uses SIGTERM(15) by default.


#### System configuration

`sudo lshw -short`

To check cpu configurations:
`lscpu`

To check storage services:
`lsblk`


### File Permissions

#### Enable/Disable users from accessing files

A file may have three types of permission: read ('r'), write ('w'), and execute ('x'). Each permission may be 'on' or 'off' for each of three categories of users: the file's owner; other people in the same group as the owner; and all others. To find out a file's mode, or permission settings, use the command `ls -l filename`. The output will be of the form:

`-rwxr-x--x 1 owner      2300 Jul 14 14:38 filename`

The string of 10 characters at the left shows the mode. The initial '-' indicates that the file is a plain file; a 'd' would indicate a directory. Characters 2-4 are, respectively, 'r', 'w', or 'x' if the corresponding permission is turned on for the owner or '-' if the permission is turned off. Characters 5-7 similarly show the permissions for the group; characters 8-10 for all others.

#### Change mode of a file/directory

To change the mode of a file, use the chmod command. The general form is:

`chmod X@Y <file1> <file2> ...`

where X is any combination of the letters 'u' (for owner), 'g' (for group), 'o' (for others), 'a' (for all; that is, for 'ugo'); @ is either '+' to add permissions, '-' to remove permissions, or '=' to assign permissions absolutely; and Y is any combination of 'r', 'w', 'x'. Examples:

To deny rwx permission for group and others -
`chmod go-rwx <file/dir>`  
