# C Compiler Working (GNU Linux)

## The Process

The Compilation is the process of converting high level language into low level language and an executable file

There are fours stages undergone in this process before generating the final output executable file, they are listed below as follows
1. Pre Processor
2. Compiler
3. Assembler
4. Linker

## The Preprocessor
There are three responsiblity for preprocessors firstly it removes all the comments from the file, replaces the macro with the values everywhere in the program and searches for the header files used in the program. The System defined header files denoted by angle brackets Ex: #include <stdio.h> are searched in the /usr/include/ directory and the user defined header files are searched in the current working directory. The user defined header files are denoted with double quotes Ex: #include "somefile.h"

Cool, let's now see with an example by running the follwing command and generate the preprocessor output file with the **.i** extension, I'm having a simple code named as happylearning.c, please refer the attached image below

![image](https://user-images.githubusercontent.com/102030901/160235506-6ab97c73-d9fe-463e-a648-169f245361bc.png)

The above is the code we are going to preprocess now, brace yourselves! Also, Also the below command is used to get the output from preprocessor

`gcc -E happylearning.c -o happylearning.i`

Once the command is executed successfully, now you should be able to fina a new file called happylearning.i in the working directory
On scrolling down to the end of the file, you'll be able to find the new modified code, where the preprocessor has done the job

![image](https://user-images.githubusercontent.com/102030901/160235616-5115c426-e4ea-43ee-bc6b-a8813bfbd828.png)

As you can see the comments and the macros have been modified.

## The Compiler

## The Assembler

## The Linker
