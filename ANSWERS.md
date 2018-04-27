## Answers

1. The main states a process may be in at any point in time on a standard Unix system are
* Start - Initial state when a process is first started/created
* Ready - The process is waiting to be assigned to a processor by the operating system
* Running - After a process is assigned by a processor by the OS scheduler, the process is set to running and the processor executes its instructions
* Waiting - Process moves into the waiting state if it needs to wait for a resource to become available
* Terminated/Exit - The process has finished its execution or is terminated by the operating system

2. A Zombie process is a process that has completed execution but still has an etry in the process table. It is created when a child process is still needed to allow the parent process to read it's child's exit status. It is "reaped" or destroyed once the exit statis read via the `wait` system call and the zombie entry is removed from the process table.

3. The job of the Scheduler in the OS is to select the jobs to be submitted into the system and to decide which process to run.

4. The benefits of the MLFQ over a plain Round-Robin scheduler are that Round Robin while very fair, may suffer from performance since CPU time is spread between many different vying processes all at once. Processis in Round-Robin also take more time overall to complete. <br><br>MLFQ on the other hand, is able to make better scheduling decisions. Rather than giving a fixed priority to each process, the MLFQ varies the priority of each process based upon it's observed behavior.