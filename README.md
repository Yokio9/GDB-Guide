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
b function_name     set breakpoint at the start of function
b file.c:5          set breakpoint in file.c at line 5
```
*note: b can be replaced with break*

### 3.  Execute
```
r                         start program with current args list
r [argument list]         start program with arguments if args not previously given
r ... <infile >outfile    start your program with input, output redirected
```
*note: r can be replaced with run*

### 4.	Execution control
```
s           go to next line and step into function calls
n           go to next line and step over function calls
c           continue program (will stop at next breakpoint)
finish      continue execution until the function returns to its caller
```
*note: s, n and c can be replaced with step, next and continue*

### 5.  Stopping program
```
q           exit program
kill        kill and restart running program (type r to restart it)
```
*note: q can be replaced with quit*

## Steps
```
show args                display argument list
set args [arglist]       specify arglist for next run
```
### Breakpoint management
```
info break                  show defined breakpoints
clear function_name         delete breakpoint at the start of function
clear file.c:5              delete breakpoint in file.c at line 5
```

### Display variables
```
p [name of varible]           show defined breakpoints
ptype [expression name]       show expression's type
display [expression name]     automatically show the value of the expression when execution stops
display                       show a list of all enabled expressions
undisplay [list number]       choose an expression to remove from the list by its number
```
*note: p can be replaced with print*
