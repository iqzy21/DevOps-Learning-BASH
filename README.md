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



   

   
   
   






