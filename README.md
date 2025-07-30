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

---

## Lesson 12: else and elif

Else allows an alternative block of code to be executed when the if condition isnt met and provides an alternative direction.

![else Statement](https://github.com/user-attachments/assets/1615b4c5-d9a7-4873-8c4d-ca96659dcd6c)

Example:

![else Example](https://github.com/user-attachments/assets/19c8ed6e-6bc4-4f6a-b99f-afd2d1a6819b)

To note then is also needed after elif:

![elif Example](https://github.com/user-attachments/assets/276972c1-f20b-465a-a265-1f2e013ef694)

---

## Lesson 13: Nested if Statements

Nested if statements allow us to create more complex structured by allowing if statements in an if statement.

![Nested if Statements](https://github.com/user-attachments/assets/9fc100af-ae49-4de6-8f2d-8dbaa4a839b0)

From this I took that the structure is very different to python for nested if statements and that fi is still needed for a nested if statement.

---

## Lesson 14: While Loops

While loops allow you to repeat block of code as long as a condition remains true or a condition becomes false.

The 3 commands used are:
- while
- do  
- done

![While Loop Structure](https://github.com/user-attachments/assets/b6ede938-fd0a-4267-814d-ee35514e4b3d)

Example:

![While Loop Example 1](https://github.com/user-attachments/assets/20372853-c36e-4ebd-95c7-ce791e0e4f1d)

While loop example:

![While Loop Example 2](https://github.com/user-attachments/assets/003d3417-c44c-457d-9921-dc301f8bdca9)

While loops are mainly used for automatic tasks and iterating data.

---

## Lesson 15: For Loops

For loops allow you to iterate code for a set amount of times you set it for.

In bash for loops have 4 key words:
- for
- in
- do
- done

![For Loop Structure](https://github.com/user-attachments/assets/9f9e601e-1fae-4431-b490-d19e6c3739eb)

Example of for loop:

![For Loop Example](https://github.com/user-attachments/assets/dac1c361-15ea-42ad-a4e6-28a1cee50bf9)

For looping an array:

![For Loop Array](https://github.com/user-attachments/assets/2f56ad99-ca31-4f92-aa6f-bc120166ab3e)

Sequence command (seq) - this just outputs a given range you input:

![Sequence Command](https://github.com/user-attachments/assets/f2187d47-c7c9-4c24-b8d3-782a3da5e4df)

---

## Lesson 16: Break and Continue

Break and continue are control statements and provide more control over your loops allowing you to interrupt iterations based on condition.

**Break** - breaks the loop regardless of where it is:

![Break Statement](https://github.com/user-attachments/assets/c325b426-c9f2-41ca-bf9a-1604571a75c4)

**Continue** - skips the current iteration at what value is set and moves onto the next:

![Continue Statement](https://github.com/user-attachments/assets/c8572441-284d-42e6-9fa3-cde7a9dcdfea)

Example break with while loop:

![Break with While Loop](https://github.com/user-attachments/assets/0770cca6-3287-4413-be6d-bea582950dac)

---

## Lesson 17: Basic Functions

Functions turn our code into modules, improve script organisation and enhance reusability. They are like mini programs in our bash scripts.

Syntax of a function is - function_name() then followed by {}:

![Function Syntax](https://github.com/user-attachments/assets/7015a85d-997b-4d29-8df3-daa7258d9d6b)

Example:

![Function Example](https://github.com/user-attachments/assets/3f532bb9-4684-4967-b448-1478943ed238)

Functions can accept parameters and you can pass data to them making them more usable:

![Function Parameters](https://github.com/user-attachments/assets/bc9441b0-9b5c-445a-80e0-756054ca5dcb)

---

## Lesson 18: Functional Parameters

There are 2 types of parameters positional and special.
A position parameter uses a local variable which the value is stored in then the variable is used by the function.

Bash provides a set of special parameters that can be accessed in functions:

![Special Parameters](https://github.com/user-attachments/assets/293267af-bee1-489a-98b7-e172dd5c209d)

Positional parameters allow us to pass data to functions and lets us access them using numbered variables like $1 and $2.
Special parameters allow us to get more info about our script by using arguments such as:
- $# to display argument number
- $0 for script name  
- $@ for all arguments

---

## Lesson 19: User Inputs

User inputs allows users to interact with the script.
Read - command used for user inputs:

![User Input](https://github.com/user-attachments/assets/73909e62-e1fc-41db-aaf0-a7ce1a8e8e3a)

Read command with command line argument both methods can be combined.

---

## Lesson 20: Handling Bad Errors

1 way to validate user input is by conditional statements to check validity of input.

---

## Lesson 21: Piping

Piping allows us to pass the output of one command as input to another and allows us to connect commands.
Piping allows us to perform advance data operations in functions and store them as variables.
| this is the pipe symbol:

![Piping Example](https://github.com/user-attachments/assets/4b1b1de0-c384-49de-a0b3-a41e33671d18)

Another example of piping using the grep and awk command to find errors:

![Piping with grep and awk](https://github.com/user-attachments/assets/3e4bdb75-5a3d-42a8-8779-366e27e61ce9)

---

## Lesson 22: Introduction to Error Handling

What is error handling? Is when you assess what can go wrong in a script and input necessary measure to handle those situations and effective error handling can save you alot of trouble.

Pre error handling:

![Pre Error Handling](https://github.com/user-attachments/assets/c608b427-e325-42fd-8fe5-a88a5df5b9e3)

Post error handling:

![Post Error Handling](https://github.com/user-attachments/assets/e38060f6-dbec-41ea-88f4-def93acb4e7b)

---

## Lesson 23: If Statement Recap for Error Handling

This is basic error handling using if and else:

![Basic Error Handling](https://github.com/user-attachments/assets/2a942cb3-415a-461d-877d-5c7c01d041e9)

---

## Lesson 24: Exit Codes

Exit code is a numerical value that tells you whether if the command or script executed has been completed or failed 0 being success anything other than 0 being an error.
The command to check this in a linux terminal is `echo $?`

![Exit Codes](https://github.com/user-attachments/assets/6b06b519-dc36-4e68-a75e-b6fa46d65c79)

Script example:

![Exit Codes Script](https://github.com/user-attachments/assets/15c7bc89-6993-4dc1-aab6-aadf66e0dee6)

---

## Lesson 25: set -e

When set -e is at the start of a script it will stop the script when a command returns a non 0 exit code:

![set -e Example](https://github.com/user-attachments/assets/7652f677-23f2-4e68-bc20-2c6ae53b37f2)

Set -e can catch errors early nullify future problems in the script.

---

## Lesson 26: set -u

Set -u forces a bash script to stop if it encounters an uninitialized variable and prevents scenarios when missing data leads to incorrect results or unexpected behaviour.

Example:

![set -u Example 1](https://github.com/user-attachments/assets/7f5059f0-e21a-45e8-a4b9-33ca055720ed)

Example with calculation:

![set -u Example 2](https://github.com/user-attachments/assets/c62dc0c9-dd0e-4fc9-8156-d9f117a5daa2)

As we can see here w is not a set variable so set-u catches it out and stops the script.

---

## Lesson 27: set -x

Set -x is a command that helps debug scripts by printing each command in the script to the terminal before it is used.
This is helpful as you can follow the flow of your script:

![set -x Example](https://github.com/user-attachments/assets/c34b8a08-577e-41c9-a77d-7fb06d82a420)

Example of it in a script:

![set -x Script Example](https://github.com/user-attachments/assets/b73e0987-3ade-47e7-af05-0935376cb780)

To debug a certain section you need both set -x and set +x:

![set -x Section Debug](https://github.com/user-attachments/assets/b4a5b5d8-f4fc-4f44-b222-5734fcfdf7ba)

---

## Lesson 28: set -eux

Bash allows us to use them all at once and I will show how they work:

![set -eux Example](https://github.com/user-attachments/assets/97e9b6df-0407-468a-baac-49a36aae53df)

---

## Lesson 29: More Set Commands

- **set -o nounset** like set -u this will also catch uninitialized variables
- **set -o errexit** like the set -e option it will look for non returned 0 numbers  
- **set -o pipefail** this causes a pipeline to return the most recent command of the pipeline that exited with non 0 status

---

## Lesson 30: Change PATH Permanently

In this lesson we learn how to change PATH directories permanently because it will only be done temporary in the terminal.
Create new directory then make script and make it executable:

![Change PATH Permanently]<img width="538" height="127" alt="image" src="https://github.com/user-attachments/assets/9f7621a4-ff04-4d08-b7d5-22f880bd874f" />


Add directory to path permanently then source 
the command we used was echo "export PATH=\$PATH:~/my_scripts":
This creates the text export PATH=$PATH:~/my_scripts, which is a command that adds ~/my_scripts to your PATH variable, while preserving the existing PATH ($PATH).

>> ~/.zshrc:
This appends the above line to your .zshrc file, which is the startup script for the Zsh shell.
<img width="595" height="145" alt="image" src="https://github.com/user-attachments/assets/92a6a872-a29f-4a2d-99f7-7d71866f9b6e" />

Now you can run from anywhere. i went to the root and ran the script<img width="162" height="114" alt="image" src="https://github.com/user-attachments/assets/d840b3e4-5721-4e57-95ad-a697d8c0c5ab" />

## Lesson 31: Reading Environment Variables
environment variables allow us to store or retrieve important information within a bash script
think of environment variables as ocntainers that hold valuable information 
environment variables have to be in capitals 

read environment variable example <img width="503" height="288" alt="image" src="https://github.com/user-attachments/assets/35f95a16-9d2e-4b1f-b550-0de3ed2baeab" /> 

## Lesson 32: Reading Environment Variables
environment variables are set variables within bash hat all have a different use below i have given some examples of this 
🧠 General Environment Variables
Variable	Description
PATH	Directories to search for executable files.
HOME	The current user’s home directory.
USER	The username of the current user.
SHELL	The path of the current user's shell (e.g., /bin/zsh, /bin/bash).
PWD	The current working directory.
OLDPWD	The previous working directory.
LOGNAME	The user's login name.
HOSTNAME	Name of the host/computer.
UID	The user ID of the current user.
EUID	The effective user ID (useful with sudo).
GROUP	Group of the current user.
EXAMPLE 
<img width="890" height="613" alt="image" src="https://github.com/user-attachments/assets/6a5b4301-1db2-420c-9af5-7e70e7ab6091" />

## Lesson 33: Reading files
Reading files is an important task in scripting. It allows us to access and extract valuable information from various types of files.
readfile loop 
<img width="701" height="578" alt="image" src="https://github.com/user-attachments/assets/8dcaad93-2fa6-45ef-80be-b3c7b4d9c546" />

file loop using cat command and processing line by line <img width="645" height="525" alt="image" src="https://github.com/user-attachments/assets/c610eaf4-937c-40af-91cb-94847391713b" />

## Lesson 34: writing files
Writing files allows us to create, modify, and store information in various formats.
under is an example of that 
<img width="668" height="362" alt="image" src="https://github.com/user-attachments/assets/7a35cd6f-1349-4cb7-b761-dedeec434e83" />
also in this lesson i learnt that 
> is to replace old data for new 
>> is to keep old data and append new data 
<img width="659" height="580" alt="image" src="https://github.com/user-attachments/assets/51799445-b5ee-48ac-abe0-4bfd95d65042" />


## Lesson 35: File Checksums
File checksums are cryptographic hashes that provide a unique fingerprint for a file, which allows us to verify the authenticity of the file.
the comman we use is md5sum and this command computes and displays the MD5 hash of a file to verify data integrity. <img width="472" height="347" alt="image" src="https://github.com/user-attachments/assets/1198ec40-6d37-46e5-8d7c-4a0d7b6a4d82" />

anotehr cammand we can use is sha256sum 
sha256sum computes and displays the SHA-256 hash of a file to verify data integrity.

CH 3 DNS
What is DNS?
DNS – Domain Name System
DNS is like a contacts list for the internet.
It allows users to access websites using domain names instead of IP addresses, which are harder to remember.
Behind the scenes, DNS translates domain names into IP addresses so devices know where to send requests.
Without DNS, users would need to manually type long IP addresses to visit websites.

Examples of how DNS helps:

Type www.google.com instead of 192.168.0.5
Helps your browser find and connect to the correct server
Acts like a phonebook for websites
Makes the internet easier and more human-friendly
<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/34ff07f2-4b72-437c-b9d3-e7a2557f74f9" />


DNS Components: Nameservers and zome files.
Name servers: 
There are 2 types authrative and recursive name servers
Authartative name servers hold th actual DNS records when quiried they provide a definite answer IP address for a domain name
Recursive name servers these servers do not hold the final answer instead they quirey other name servers on behald of the cluient to fidn the correct DNS Record they can also catch the information they retrived to speed up queries

pratical finding DNS server of a domain 
Dig ns (domain)
<img width="857" height="612" alt="image" src="https://github.com/user-attachments/assets/1b36289a-4db8-4e02-8d9e-3497290a1176" />

the commands just to get DNS
dig +short ns (domain name)
<img width="1078" height="205" alt="image" src="https://github.com/user-attachments/assets/44de7897-a6f9-4477-b5eb-be2ec7833bee" />

Zone files:
zone files are stored inside your name service and they contain information about the domain
They help name servers answer queries about how to get tooa  domain if the name server doesnt know the answer directly 
Zone files organise you DS information in a readable and managed way making it easier to handle 
<img width="1960" height="1250" alt="image" src="https://github.com/user-attachments/assets/9ce273ac-791e-4bb3-a03e-2a25d748b74e" />

DNS Components: records 
Az zone file is composed of many records 
Each record contains specific information about hosts, names servers and other recourses 
Resource components: Record names,TTL, Class, TYpe, data 
Record name - domain name being quired
Time to live (TTL) indicates how long a record is valid before refresh required
Class - name space of the record information 
Type - type of record (A or MX or AAAA etc)
NS - name server record
data - The actual information corresponding to the record type. Like IP address for an A record
<img width="656" height="246" alt="image" src="https://github.com/user-attachments/assets/2d36c599-d0cb-464c-afca-ff64f8cfaf76" />

DNS records:
A – Maps a domain name to an IPv4 address.
AAAA – Maps a domain name to an IPv6 address.
CNAME – Alias of one name to another. It allows you to point multiple domain names to the same IP address.
MX – Specifies the mail server responsible for receiving email for the domain.
TXT – Allows domain administrators to insert any text into DNS.
Commonly used for:
Verification purposes
Holding SPF (Sender Policy Framework) data
<img width="744" height="207" alt="image" src="https://github.com/user-attachments/assets/12a1c57e-e1dc-46b8-8faa-46d97aa8289f" />

A record example - most common type of dns record and essential for directing trafic to the correct ip address 
<img width="611" height="114" alt="image" src="https://github.com/user-attachments/assets/69c633ee-4f08-44b7-a7fb-134c929c1fdc" />

AAAA record example - same as above but less common
<img width="615" height="116" alt="image" src="https://github.com/user-attachments/assets/9a19ae8d-da7f-4a0c-b3e4-cd12c7982fe7" />

CNAME record example - this create and alias for your domain name makes DNS managment easier by allwoing you to point different domain names to 1 IP address 
<img width="600" height="137" alt="image" src="https://github.com/user-attachments/assets/5ff46f63-919b-4a28-9014-c4c59a65f8be" />

MX record example - essential for routing emails to the correct mail servers ensuring email delibvery is reliable
<img width="601" height="141" alt="image" src="https://github.com/user-attachments/assets/057fc3ac-c30b-446f-a4d9-cbbd103fe102" />

TXT record - one of the main purposes is to verify you own the domain but also has many purposes 
<img width="603" height="137" alt="image" src="https://github.com/user-attachments/assets/434f4676-4f2c-420f-a0aa-a0edad270fc1" />

How DNS works:
What is DNS resolution:
DNS resolution is the process of converting domain names into IP addresses 
DNS break down:
DNS Route (the boss) - This is the top of the hierchary, it doesnt store details about specific domains, but rather keeps high level informaion on where to find the top-level domains underneath it.

TLD'S Top Level Domains - These are liek calling your departnment heads they include familiar extentions such as .com, .org
, .net 
Each TLD stores information about domains within the cope

Authoritive name servers Host+Zones for domains - This is where the details DS records for those domains for example google.com have their own records stored in here 

Domain - each domain gas a zone and zone file where the zone is like a team within a departnemnt and the zone file is a detailed list of information

This is where imformations such as IP addresses, mail servers of the domains are stored



