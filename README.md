# GDB-Guide

## Steps

### 1.  Launch
!!! Remember to compile program with -g
```
gdb ./name_of_executable                        Launch without arguments
gdb --args ./name_of_executable [arguments]     Launch with arguments
```
### 2.  Add a breakpoint
```
b function_name                                 set breakpoint at start of function
b file.c                                        set breakpoint at
```
*note: b can be replaced with break*

### 3.  Execute
```
r                                               start program with current args list
r [argument list]                               start program with arguments if args not previously given
r ... <infile >outfile                                start your program with input, output
redirected
```
### 4.  execution control
