# GDB-Guide

## Steps

### 1.  Launch debugging
Compile program with -g

|gdb ./name_of_executable|Launches without arguments|
gdb --args ./name_of_executable [arguments]     Launches with arguments

### 2.  add a breakpoint
b function_name                                 sets breakpoint at start of function
b file.c                                        sets breakpoint at

*note: b can be replaced with break*

### 3.  start debugging
r                                               starts debbuging
r [argument list]                               starts debbuging with arguments if args not previously given

### 4.  execution control
