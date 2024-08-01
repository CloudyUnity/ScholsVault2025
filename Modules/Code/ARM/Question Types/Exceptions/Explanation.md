Exceptions are events outside the expected flow of execution of a program
During an exception or interrupt the contents of all registers are saved onto the stack and a subroutine is called
After exiting the program resumes as normal unless the subroutine had a breakpoint or something
The processor knows to do this by the exception storing a specific value in LR to tell it to restore all registers
The processor uses the exception vector table to find what subroutine to call in the event of each exception