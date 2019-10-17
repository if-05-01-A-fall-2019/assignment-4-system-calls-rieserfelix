###Systemcalls

#-fork:
creates a new process (child process) that shall be an exact copy of the calling process (parent process)
if fork() returns negative value, the creation of a child process was unsuccesful

fork() returns 0 to the newly created child process

fork() reutrns a positive value, the process ID of the child process, to the parent. the returned process ID is of type pid_t defined in sys/types.h
>fails if
->[ENOMEM]
Not enough storage space is available.

#-stat: 
The stat() function gets information about the named file and write it to the area pointed to by the buf argument (schreibt sie in den Bereich, auf den das Argument buf verweist).The path argument points to a pathname naming a file.

#-kill: 
send a signal to a process or a group of processes specified by pid operands

>fails if
->[EINVAL]
The value of the sig argument is an invalid or unsupported signal number

#-mmap: 
creates a new mapping in the virtual address space of the
calling process.
-chmod: changes the file mode bits of each given file according to mode.

>  fails if
->[EINVAL]
The value of the mode argument is not valid.

-waitpid wait for a child process to stop or terminate

The waitpid() functions shall obtain status information pertaining to one of the caller's child processes. Various options permit status information to be obtained for child processes that have terminated or stopped.

##Fail Conditions

#-exec:
>fails if
-> [EACCES] 
The new process file is not an ordinary file and the implementation does not 	 	   support execution of files of its type.                                                                                

#-unlink:   
>fails if
->[ENOTDIR]
A component of the path prefix is not a directory.


#-read:      
fails if
->[EIO]
A physical I/O bug has happened .
#-mount:  
>fails if
->[EBUSY]  
Source cannot be remounted read-only, because it still holds
files open for writing.

#Trap
To switch between user mode and kernel mode. It acts like a function call but it jumps onto a specific address in the kernel space and switches into the kernel mode


