# statsThread

Team members: Daniel Hernandez, Rudy Leiva

How to compile:

Linux/UNIX & Mac OS X:
Part 1 - stats.c
Open terminal, cd to the directory where the source code file is stored. Run "gcc -o stats stats.c" (without quotes) on the terminal window. To run the program, simply do "./stats [list of numbers delimited by the space character]" (without quotes) (replace [] with actual integer numbers).

Part 2 - statsThread.c
Open terminal, cd to the directory where the source code file is stored. Run "gcc -o statsThread statsThread.c -pthread" (without quotes) on the terminal window. To run the program, simply do "./statsThread [list of numbers delimited by the space character]" (without quotes) (replace [] with actual integer numbers).

Windows (Any version): Part 1 & Part 2 NOT COMPATIBLE - The use of fork() and pthread() functions are only available in Linux/UNIX.

Files included:

stats.c (source code) (Part 1)
statsThread.c (source code) (Part 2)
stats (C executable file) (Part 1)
statsThread (C executable file) (Part 2)

Description / Purpose of Program:

Part 1
Project 2 (Part 1): This program is passed command line arguments at the time of execution. The program goes through the all the arguments to get a count of how many valid arguments were provided. Anything that isnt a valid argument is excluded from this count. If no arguments are passed in the command line or all the arguments passed were not valid, some information is displayed on how to properly execute this program and the program will terminate at that point. Once there is a count, an array of integers is created to hold the number of elements given by the value of count. Then the program goes through each command line argument and for each argument that is a valid number, it will be converted from character to integer and added to the integer array. Next, the fork() function is used to create new processes that will performe the required statistical calculations for average, minimum, and maximum value.

Part 2
Project 2 (Part 2): This program is passed command line arguments at the time of execution. The program goes through the all the arguments to get a count of how many valid arguments were provided. Anything that isnt a valid argument is excluded from this count. If no arguments are passed in the command line or all the arguments passed were not valid, some information is displayed on how to properly execute this program and the program will terminate at that point. Once there is a count, an array of integers is created to hold the number of elements given by the value of count. Then the program goes through each command line argument and for each argument that is a valid number, it will be converted from character to integer and added to the integer array. Next, the program creates 3 threads using the pthread_create() function. Each thread is provided a seperate pthread_t variable, NULL for attributes, a pointer to a different function, and pointer to the integer array (the pointer is a void * and is then cast back into an int). Each thread then performs its calculation and each result is ouput by the appropriate thread while the main thread waits for the other to complete. When all threads are completed, they are joined back to the main thread and the program will end successfully.

Team member contributions:

Daniel Hernandez -

code development
code debugging
error handling
research fork() function
research pthread_join()
research on function atoi()
reasearch on taking command line arguments
README
stats.c
statsThread.c

Rudy Leiva -

code development
code debugging
error handling
research pthread() function (pthread_create)
research/review on pointers
research on taking command line arguments
stats.c
statsThread.c
