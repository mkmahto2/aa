# shell programming
A shell script is a computer program designed to be run by the Unix/Linux shell which could be one of the following:

The Bourne Shell
The C Shell
The Korn Shell
The GNU Bourne-Again Shell
A shell is a command-line interpreter and typical operations performed by shell scripts include file manipulation, program execution, and printing text.

~~~
#!/bin/sh


echo "What is your name?"
read PERSON
echo "Hello, $PERSON"
~~~

Shell Prompt
The prompt, $, which is called the command prompt, is issued by the shell. While the prompt is displayed, you can type a command.

Shell reads your input after you press Enter. It determines the command you want executed by looking at the first word of your input. A word is an unbroken set of characters. Spaces and tabs separate words.

Following is a simple example of the date command, which displays the current date and time −
~~~
$date
Thu Jun 25 08:30:19 MST 2009
~~~
# Shell Types
In Unix, there are two major types of shells −

Bourne shell − If you are using a Bourne-type shell, the $ character is the default prompt.

C shell − If you are using a C-type shell, the % character is the default prompt.

## The Bourne Shell has the following subcategories −

Bourne shell (sh)
Korn shell (ksh)
Bourne Again shell (bash)
POSIX shell (sh)
## The different C-type shells follow −

C shell (csh)
TENEX/TOPS C shell (tcsh)

Example Script
Assume we create a test.sh script. Note all the scripts would have the .sh extension. Before you add anything else to your script, you need to alert the system that a shell script is being started. This is done using the shebang construct. For example −
~~~
#!/bin/sh
~~~
This tells the system that the commands that follow are to be executed by the Bourne shell. It's called a shebang because the # symbol is called a hash, and the ! symbol is called a bang.

To create a script containing these commands, you put the shebang line first and then add the commands −
~~~
#!/bin/bash
pwd
ls
~~~
Shell Comments
You can put your comments in your script as follows −
~~~
#!/bin/bash

# Author : mukesh
# Copyright (c) mukesh
# Script follows here:
pwd
ls
~~~
Save the above content and make the script executable −
~~~
$chmod +x test.sh
~~~
The shell script is now ready to be executed −
~~~
$./test.sh
~~~
Upon execution, you will receive the following result −
~~~
/home/mukesh
index.htm  unix-basic_utilities.htm  unix-directories.htm  
test.sh    unix-communication.htm    unix-environment.htm
~~~
This (. ) Dot Is represented the present working directory. We can write the present working directory instead of (.) Dot
## Variable Names
The name of a variable can contain only letters (a to z or A to Z), numbers ( 0 to 9) or the underscore character ( _).

By convention, Unix shell variables will have their names in UPPERCASE.
The following examples are valid variable names −
~~~
_ALI
TOKEN_A
VAR_1
VAR_2
~~~
Following are the examples of invalid variable names −
~~~
2_VAR
-VARIABLE
VAR1-VAR2
VAR_A!
~~~
