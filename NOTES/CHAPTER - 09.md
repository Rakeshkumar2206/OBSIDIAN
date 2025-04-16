**Security Vulnerabilities, Threats and Countermeasures***

**Multiprocessing** - More than one processor is used to complete the execution of a multi threaded application

**Multiprogramming** - It is similar to multitasking where it can handle two tasks on a single processor coordinate by the OS. 

**Multithreading** - Multithreading permits multiple concurrent tasks to be performed within a single process. 

**Process States**
It is a state where the OS is concerned, it can in one of two modes at any given moment, operating in a privileged, all access mode known as supervisor state or operating in what's called the problem state associated with user mode, where privileges are low and all access requests must be checked against credentials for authorization before they are granted or denied.

**Ready** - In the ready state, a process is ready to resume or begins its processing as soon as it  is scheduled for execution.

**Running**- In the Running State of problem state is when a process executes on the CPU and Keeps going until it finishes its time slice expires, or it is blocked for some reason. If the time slice ends and the process isn't completed, it returns to the ready state, if the process is paused while waiting for I/O, it goes into the waiting state.

**Waiting** - The waiting state is when a process is ready for continued execution but is waiting for I/O to be serviced before it can continue processing. Once I/O is complete then the process typically returns to the ready state, where it wait is in the process queue to be assigned time again on the CPU for further processing.

**Supervisory** - The Supervisory state is used when the process must perform an action that requires privileges that are greater than the problem states set of privileges, including modifying system configuration, installing device drivers, or modifying security settings. Basically any function not occurring in the user mode or problem state takes place in the supervisory mode. This state is not shown, but it effectively replaces the running state when a process is run with higher level privileges.

**ROM** - Read Only Memory works like the name implies- its memory the system can read but cant change (No writing Allowed). The contents of a standard ROM Chip are burned in at the factory and the end user simply cannot alter it. 
	- Programmable Read Only Memory (PROM) - A basic programmable read-only memory chip is similar to a ROM chip in functionality, but with one exception. During the manufacturing process a Prom chips content are not  burned in a  the factory as with standard ROM chips. Instead a prom incorporates special functionality that allows an end user to burn in the chip's contents later. Once data is written to a PROM chip, no further changes are possible.
	
**Random & Sequential**
 *Random* Access storage devices allow an OS to read and sometimes write immediately from any point within the device by using some type of addressing system. Almost all primary storage devices are random access devices. Eg RAM
 *Sequential* devices has to go through all the physical devices stored prior to the desired location. A common example of a sequential device is a magnetic tape drive.

**Direct Addressing** 
In the Direct addressing, the CPU is provided with an actual address of the memory location to access. 

**Emanation Security**
Adversaries can intercept electromagnetic or radio frequency signals (Collectively known as emanations) from these devices and interpret them to extract confidential information