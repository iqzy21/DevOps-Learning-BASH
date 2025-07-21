# Bash Scripting Learning Guide

## Lesson 1: Introduction to Bash

### What is Bash?
Bash is a programming language that is used in linux terminals and is a command line tool that interacts with your computer.

### Bash Script
Bash script is a file containing a series of commands you want the computer to execute.

### Why Should Bash be Learned for DevOps?
1. Tasks can be automated to save time
2. Scripts can handle files, software installs and system configurations  
3. Importantly boosts work efficiency saving time on different processes

---

## Getting Started: Bash Commands

### 1. Shebang (#!):
The first line in your file should be `#!/bin/bash` - This tells the computer to use bash to run a script

### 2. Running Your Script: 2 Main Commands
- `chmod +x your_script.sh` - this linux command makes your script executable
- `./your_script.sh` - This command runs your script

### 3. Basic Concepts:

#### Variables:
`variable=""` is used to store values  
e.g `name="iqzy"`

`echo "(anything), $variable"` is to use the variable  
e.g `echo "Hello, $name"`  
$ is how variables are assigned to be used in a command

#### Comments:
Add explanations with #.  
e.g `#this line says hello`  
Comments are ignored by the terminal and just seen as plain text

#### Conditionals:
Making decisions with if statements  
e.g `if [ $name == "iqzy" ]; then echo "Hi Alice!"`  
Use if statements to run commands based on conditions.

#### Loops:
Repeat actions with for or while:  
e.g `for i in 1 2 3; do echo "Number $i" done`  
e.g `i=1; while [ $i -le 3 ]; do echo "Number $i"; i=$((i+1)); done`  
Use for or while to repeat a block of code multiple times.

#### Functions:
Group commands for reuse.  
e.g `greet() { echo "Hello, $1!" } greet "Alice"`  
Define reusable blocks of code with a name and optional parameters.

#### User Input:
Get input from users.  
e.g `read -p "Enter your name: " name echo "Hello, $name!"`  
Use read to get input from the user and store it in a variable.

### Tips
- Start small: Write simple scripts first.
- Use meaningful names: This makes your script easier to understand.
- Test often: Avoid surprises by running your scripts frequently.

### Practice Makes Perfect!
The more you script, the better you get. Try automating small tasks daily.
Bash scripting becomes easier with repetition—keep at it!

![Bash Introduction](https://github.com/user-attachments/assets/7d529f1f-59fb-4cfc-89b3-10af3623c820)

---

## Lesson 2

.sh shows that it is a bash script

---

## Lesson 3

She bang serves as a directory to the operating system on how to interpret a script and in this case its asking the system to interpret the script using binary bash and she bang allows flexibility and tells the OS what language model to use.

### 3 Ways to Run Bash Commands
- `./yourfile.sh`
- `sh yourfile.sh`  
- `bash yourfile.sh`

![Running Bash Scripts](https://github.com/user-attachments/assets/261740b4-236f-4c97-b7fe-cdfffe047871)

She bang #! is not limited to bash and can be used for different languages, it specifies the interpreter of shell that should be used for your script, it enables consistent executable scripts on different environments regardless of shell you are using should be placed as first line of the script.

---

## Lesson 4a: Comments

Comments are lines in a script that are not executed however they serve the purpose for clarity and help understand your script and its used with best practices for this reason.

In bash there is 2 types of comments single line and multi line:

### Single Line Comments
`#` is used to create single line comments

![Single Line Comments](https://github.com/user-attachments/assets/0ed47fa9-4f1a-413b-bcad-ee9665908a27)

### Multiline Comments
First `:` is used then a space and `'` this is to start off your multiline after you use another `'` to close your multiline so anything between 6 and 9 on the image is a comment

![Multiline Comments](https://github.com/user-attachments/assets/2a1ee55e-55b1-42e9-abc9-0c440351f36e)

As you can see here the final example:

![Comment Example](https://github.com/user-attachments/assets/dec11f69-154d-4fa4-b293-c1d9b6e50ab7)

### Practical Benefit Example
Here is a script that can look a bit hard to understand for someone new to bash scripting:

![Script Without Comments](https://github.com/user-attachments/assets/7c70a6bc-55fb-4701-99da-d87080bccbc1)

Now here is a commented example:

![Script With Comments 1](https://github.com/user-attachments/assets/940f31bd-763e-4db5-88cb-f3e218cb61bc)

![Script With Comments 2](https://github.com/user-attachments/assets/a1932871-a545-4839-805d-2ba6fb76ed1f)

---

## Lesson 4b: Running Scripts Anywhere

PATH command is an environmental that tells the shell to search for directories that can allow us to run scripts from anywhere:

![PATH Environment Variable](https://github.com/user-attachments/assets/aaa6fabe-d646-44c4-b8f9-885f0f885200)

Any executable files placed in these directories can be ran from anywhere and the best place to put scripts is in `/usr/local/bin/` and I have also changed the name to make it easier to run and u can see this in the image:

![Global Script Example](https://github.com/user-attachments/assets/f82867ab-03cd-4076-a1e8-9b7ce19aa151)

Ensure the scripts u add to global paths are safe to use and are for global purposes.

---

## Lesson 5: Variables

In bash variables are like containers that hold data and they are assigned with `=`.  
To use the variable you have to use `$` before the variable name and use a command to access that variable:

![Variable Assignment](https://github.com/user-attachments/assets/8a081451-14a6-4bf0-ae25-5e2bd6a936a2)

Heres some example of examples of variable uses:

![Variable Examples](https://github.com/user-attachments/assets/19c13b98-d1ea-417f-9c27-a9809137b8d7)

---

## Lesson 6: Parameters

Parameters are known as input values and can be passed into a script by allowing inputs in the command line it can make your script more versatile and interactive.

Bash scripts can receive parameters from the command line when executed and allow you to customise the behaviour of your script making it more flexible.

Here I have made 3 parameters. Parameters are accessed by using `$1` `$2` `$3` and so on:

![Parameter Definition](https://github.com/user-attachments/assets/b49610cb-a133-425f-8688-119594cb5185)

And you can see here them being passed. Now to pass an input to the parameters you just have to write what you want after your sh command:

![Parameter Usage](https://github.com/user-attachments/assets/fc01ab4e-f8c4-483f-a4e2-65ad068b7b40)

To access all parameters you do the same thing but use `$@`:

![All Parameters Symbol](https://github.com/user-attachments/assets/099d7559-40ea-4e9e-bb60-9a64c59d3e00)

Now you can see here it being used:

![All Parameters Usage](https://github.com/user-attachments/assets/1300475a-ee46-451c-8cd3-35eb552b4c22)

---

## Lesson 7: Arithmetic Expansion
bash provides a straighforward way to do mathmatic calcyulations by using $((  ))<img width="526" height="295" alt="image" src="https://github.com/user-attachments/assets/2dd3332f-d170-4d6d-86de-4b36d7e71f45" />
<img width="367" height="329" alt="image" src="https://github.com/user-attachments/assets/5a3ffe8d-e10a-4631-844c-61fc7427645e" />

## Lesson 8: Arithmetic expansion (With Parameters)
same thing as lesson 7 instead of a value you just put $(number)
how ever i learnt that if you run the script it wont prompt you to add numbers like python you have to put the numbers ur self in the command 
<img width="434" height="375" alt="image" src="https://github.com/user-attachments/assets/8fa36867-0a51-4a3e-809e-6a67392ebed2" />

## Lesson 9 and 10: install vs code 
alrerady did that

## Lesson 11: if statements
if statments starts with if then ends with fi inbetween them there is a then 
when the if condition is true the code between then and fi will execute 

comparison operators
eq = equals or ==
ne = not equal to !=
lt = less than < with []
gt = greater than > with []
le = less than or equal to 
get =  greater than r equal to
if conditions have to be placed in [] 
<img width="392" height="275" alt="image" src="https://github.com/user-attachments/assets/4688cf6b-cf10-4786-a999-b71acf939ff3" />

logical operators logical operators help make scripts make more decisions 
&& = and
|| = or
<img width="586" height="313" alt="image" src="https://github.com/user-attachments/assets/865d0dfa-934a-4479-a644-39257f88c79b" />

## Lesson 12: else and elif 
else allows an altervnitive block of code to be executed when the if condition isnt met and provides an alternitive direction 
<img width="323" height="133" alt="Screenshot 2025-07-21 191048" src="https://github.com/user-attachments/assets/1615b4c5-d9a7-4873-8c4d-ca96659dcd6c" />
example <img width="298" height="298" alt="image" src="https://github.com/user-attachments/assets/19c8ed6e-6bc4-4f6a-b99f-afd2d1a6819b" />

to note then is also needed after elif <img width="397" height="440" alt="image" src="https://github.com/user-attachments/assets/276972c1-f20b-465a-a265-1f2e013ef694" />

## Lesson 13: nested if statments 
nested if statments allow us to create more complex structured by allowing of statments in an if statment 
<img width="454" height="327" alt="image" src="https://github.com/user-attachments/assets/9fc100af-ae49-4de6-8f2d-8dbaa4a839b0" />
from this i took that the structure is very different to python for nested if statments and that fi is still needed for a nested if statment 

## Lesson 14: while loops
while loops allow you to repeat block of code aslong as a condition remains true of a condition becomes false 

the 3  commands used are 
while
do
done <img width="303" height="136" alt="image" src="https://github.com/user-attachments/assets/b6ede938-fd0a-4267-814d-ee35514e4b3d" /
example
<img width="484" height="515" alt="image" src="https://github.com/user-attachments/assets/20372853-c36e-4ebd-95c7-ce791e0e4f1d" />
while loop example <img width="755" height="461" alt="image" src="https://github.com/user-attachments/assets/003d3417-c44c-457d-9921-dc301f8bdca9" />

while loops are mainly used for automatic tasks and itterating data 

## Lesson 15: foor loops
foor loops allow you to iterrate code for a set amount of times you set it for 
in bash for loops have 4 key words
for 
in
do
done
<img width="284" height="114" alt="image" src="https://github.com/user-attachments/assets/9f9e601e-1fae-4431-b490-d19e6c3739eb" />

example of for loop<img width="764" height="338" alt="image" src="https://github.com/user-attachments/assets/dac1c361-15ea-42ad-a4e6-28a1cee50bf9" />

for looping an array
<img width="331" height="349" alt="image" src="https://github.com/user-attachments/assets/2f56ad99-ca31-4f92-aa6f-bc120166ab3e" />

sequence command - this justout puts a given range you input


