lesson 1 introduction to bash:

what is bash: bash is a programming language that is used in linux terminals and is a command line tool that interacts with yout computer 
Bash Script: bash script is a file contaning a series of commands you want the computer to execute

why should bash be learened for devops?:
    1. tasks can be automated to save time
    2. scripts can handle files, software installs and system configurations
    3. importantly boosts work efficency saving time on different processes 

Gettng started : bash commands
1. Shebang (#!):
   The first line in your file should be #!/bin/bash - This tells the computer to use bash to run a script

2. running your script: 2 main commands
   chmod +x your_script.sh - this linux command makes your script executable
   ./your_script.sh - This command runs your script

3. Basic concepts:
   Variables:
   variable="": is used to store values
   e.g name="iqzy"

   echo "(anything), $variable": is to use the variable
   e.g echo "Hello, $name"
   $ is how variables are assigned to be used in a command

   Comments:
   Add explanations with #.
   e.g #this line says hello
   comments are ignored by the terminal and just seen as plain text

   Conditionals:
   Making decissions with if statments
   e.g if [ $name == "iqzy" ]; then echo "Hi Alice!"
   Use if statements to run commands based on conditions.

   Loops:
   Repeat actions with for or while:
   e.g for i in 1 2 3; do echo "Number $i" done
   e.g i=1; while [ $i -le 3 ]; do echo "Number $i"; i=$((i+1)); done
   Use for or while to repeat a block of code multiple times.

   Functions:
   Group commands for reuse.
   e.g greet() { echo "Hello, $1!" } greet "Alice"
   Define reusable blocks of code with a name and optional parameters.
   
   User input:
   Get input from users.
   e.g read -p "Enter your name: " name echo "Hello, $name!"
   Use read to get input from the user and store it in a variable.

Tips
Start small: Write simple scripts first.
Use meaningful names: This makes your script easier to understand.
Test often: Avoid surprises by running your scripts frequently.

Practice Makes Perfect!
The more you script, the better you get. Try automating small tasks daily.
Bash scripting becomes easier with repetition—keep at it!

<img width="802" height="569" alt="image" src="https://github.com/user-attachments/assets/7d529f1f-59fb-4cfc-89b3-10af3623c820" />

lesson 2
.sh shows that it is a bash script 

lesson 3
she bang serves as a directory to the operating system on how to interprate a script and in this case its asking the system to interprate the script using binary bash 
and she bang allows flexibility and tels the OS what language model to use
3 ways to run bash commans
./(yourfile).sh
sh (yourfile).sh
bash (yourfile).sh
<img width="348" height="362" alt="image" src="https://github.com/user-attachments/assets/261740b4-236f-4c97-b7fe-cdfffe047871" />

she band #! is not limited to bash and can be used for different languages, it specifies the interprature of shell that should be used for your script, it enables conistent excecutable scripts on different environments regarless of shell you are using should be placed as first line of the script 

lesson 4a comments
comments are lines in a script that are not executed how ever they serve the purpose for clarity and help undrstand your script and its used with best practices for this reason 
in bash there is 2 types of comments single line and multi line
single line: # is used to create single line comments 
<img width="487" height="164" alt="image" src="https://github.com/user-attachments/assets/0ed47fa9-4f1a-413b-bcad-ee9665908a27" />

multiline: first : is used then a space and ' this is to start off your multiline after you use another ' to close your multiline so anything between 6 and 9 on the immage is a comment
<img width="456" height="136" alt="image" src="https://github.com/user-attachments/assets/2a1ee55e-55b1-42e9-abc9-0c440351f36e" />

as you can see here the final example
<img width="375" height="385" alt="image" src="https://github.com/user-attachments/assets/dec11f69-154d-4fa4-b293-c1d9b6e50ab7" />

pratical benefit example 
here is a script that can look abit hard to understand for some one new to bash scripting
<img width="540" height="185" alt="image" src="https://github.com/user-attachments/assets/7c70a6bc-55fb-4701-99da-d87080bccbc1" />
now here is a commented example<img width="537" height="303" alt="image" src="https://github.com/user-attachments/assets/940f31bd-763e-4db5-88cb-f3e218cb61bc" /><img width="516" height="246" alt="image" src="https://github.com/user-attachments/assets/a1932871-a545-4839-805d-2ba6fb76ed1f" />

lesson 4b running scripts any where 
PATH command is an environtmental that tells the shell to search for directories that can allow us to run scripts from any where <img width="818" height="89" alt="image" src="https://github.com/user-attachments/assets/aaa6fabe-d646-44c4-b8f9-885f0f885200" />
any executable files placed in these directories can be ran from anywhere and the best place to put scripts is in 
/usr/local/bin:
and i have also changed the name to make it easier to run and u can see this in the image<img width="566" height="144" alt="image" src="https://github.com/user-attachments/assets/f82867ab-03cd-4076-a1e8-9b7ce19aa151" />
ensure the scripts u add to global paths are safe to use and are for global purposes

lesson 5 variables
in bash variables are like containers that hold data and they are assigned with =
To use the variable you have to use $ before the variable name and use a command to access that variable<img width="325" height="216" alt="image" src="https://github.com/user-attachments/assets/8a081451-14a6-4bf0-ae25-5e2bd6a936a2" />

heres some example of examples of variable uses <img width="420" height="270" alt="image" src="https://github.com/user-attachments/assets/19c13b98-d1ea-417f-9c27-a9809137b8d7" />

lesson 6 parameter
paramaters are known as input values and can be passed into a script
by allowing inputs in the command line ti can make your script more versaile and interactive 
bash scripts can recieve paramaters from the command line when executed and allow you to customise the behaviour of your script making it more flexible

here i have made 3 parameters paramaters are accesed by using $1 $2 $3 and so on <img width="352" height="177" alt="image" src="https://github.com/user-attachments/assets/b49610cb-a133-425f-8688-119594cb5185" />
and you can see here them being passed now to pass an input to the parameters you just have to write what you want after your sh command <img width="343" height="128" alt="image" src="https://github.com/user-attachments/assets/fc01ab4e-f8c4-483f-a4e2-65ad068b7b40" />

to access all peramaters you do the same thing but use $@<img width="287" height="61" alt="image" src="https://github.com/user-attachments/assets/099d7559-40ea-4e9e-bb60-9a64c59d3e00" />
now you can see here it being used <img width="364" height="119" alt="image" src="https://github.com/user-attachments/assets/1300475a-ee46-451c-8cd3-35eb552b4c22" />

lesson 7 arithmatic operations 












   
   
   






