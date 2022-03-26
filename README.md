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
The Compiler now converts the Preprocessor Output **.i** to **.s** output which is the assembly language. This can be achieved by running the following command

`gcc -s happylearning.i -o happylearning.s`

![image](https://user-images.githubusercontent.com/102030901/160237014-ad30b740-65b6-4ec5-a9e4-3e99164cbe86.png)

So, this is the Assembly language for the program written by us.

## The Assembler
Now, let's gear up for the object binary file creation. The object binary file can be created from the Compiler output using the below command. Also, note that the object files can't be opened using vim editor as vim editor supports only the ASCII Standard Text and not Hex Code, which is used by the object files.

`gcc -c happylearning.s -o  happylearning.o`

Now you should be able to see the object file in the current working directory but wait this is not the final object file that you can execute, this still contains some missing links and missing libraies.

## The Linker
The Linker is the final process in the Compilation Process, the linker combines and maps the previous output object file with other dependent libraries, object code information and other object binary files.

`gcc happylearning.o -o runnable.o`

Now you should be able to execute the command and see the output by using the below command

`./runnable.o`
