# Linux_Kernel_Programming-C-
Linux kernel modules load,execute and remove
*The C program DFS_taskslist.c, unlike any ususal C program interacts with the kernel. It loads and unloads a module from the kernel. Kernel functions are invoked to perform the desired actions. Specifically, this program lists all the current tasks in the Linux system. 

*"task_struct” is the struct that represents PCB in the operating system.Initially, the program uses this task_struct to list all the processes one by one, created right from init   . To be specific, the iterator tasklist_iterator() lists the process name,pid and its state.

*The second portion of this program involves iterating over all tasks in the system using a depth-first search (DFS) tree. The function DFS() is recursive which is  called with the init_task as the initial parameter from the init() module. DFS tree of tasks is then created through recursive calls to DFS() where the task points iteratively to the previous task’s children or sibling each time.
*DFS_tasklist_exit() is the module exit poit that is invoked to remove the module from the kernel.

*The files KERNEL_LOG_BUFFER and ps_command_output are the output references

