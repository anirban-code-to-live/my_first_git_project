## Useful Linux Commands

#### CPU Usage and Running Process

`top`

Press 'i' to off the idle process visibility, 'M' for sort the processes in memory usage, 'S' for running time.<br/> 

`htop`

`ps aux | grep -i anirban`

The advantage of **ps** command is one can easily find processes associated with the term *anirban*

`pidof anirban`

`pgrep anir`

The commands like *top* and *ps* help to find all the running and idle processes in your system. If you happen to know the process name (or part of a process name), you can use *pidof* (*pgrep*) command.<br/>


#### Kill a process

`kill -9 <process_id>`

You can use -9 or -SIGKILL to kill the process immediately. If you dont write any of these flags, the system uses SIGTERM(15) by default.


#### System configuration

`sudo lshw -short`

To check cpu configurations:
`lscpu`

To check storage services:
`lsblk`
