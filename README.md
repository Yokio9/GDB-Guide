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
r [argument list]         start program with arguments if args not previously specified
r ... <infile >outfile    start your program with input, output redirected
```
*note: r can be replaced with run*

### 4.	Execution control
```
s                      go to next line and step into function calls
n                      go to next line and step over function calls
c                      continue program (will stop at next breakpoint)
finish                 continue execution until the function returns to its caller
until [line number]    run until the specified line
set var x = 10         change value of x to 10 during runtime
```
*note: s, n and c can be replaced with step, next and continue*

### 5.  Stopping program
```
q        exit program
kill     kill and restart running program (type r to restart it)
```
*note: q can be replaced with quit*

## Useful to know

### Display variables
```
p [name of variable]        print value of a variable
ptype [variable name]       show expression's type
display [variable name]     automatically show the value of the variable when execution stops
display                     show a list of all enabled expressions
undisplay [list number]     choose a variable to remove from the list by its number
```
*note: p can be replaced with print*

### Arguments management
```
show args              display the current argument list for the program
set args [arglist]     specify arglist for next run
```
### Breakpoint management
```
info break              show all defined breakpoints
clear function_name     delete breakpoint at the start of function
clear file.c:5          delete breakpoint in file.c at line 5
```
## Program crash cheat code 🤯💥
```
bt     print the function calls leading to the crash
```
If code crashes run bt. It will print something like this:

    #0  third_function () at test.c:6
    #1  second_function () at test.c:10
    #2  first_function () at test.c:14
    #3  main () at test.c:18
Each line shows:

    Function name (third_function, second_function, etc.)
    Source file and line number (test.c:6 means it crashed at line 6)
    The order of function calls before the crash.
