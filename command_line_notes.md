Command Line Notes
===================

Reference URLs:




|   |   |   |   |   |
|---|---|---|---|---|
|   |   |   |   |   |
|   |   |   |   |   |
|   |   |   |   |   |


$ pwd  

print working directory



ls

List files within that directory



ls -a

Lists files with 'option' which shows . & .. files



ls -t

Lists files in order of time of last modified



ls -l

Lists files in a table with  

1) access rights telling what actions are permitted on the file

2) number of hard links, or number of child directories and files including the parent link (..) and the direct link ( . )

3) the username of the file's owner

4) the name of the group that owns the file

5) the size of the file in bytes

6) the date & time that the file was last modified

7) the name of the file or directory



ls –alt

Lists all of the above, stacked, including hidden files



cd  

Change directory, Moves to another directory, if nothing after goes to root



cd ..

Goes one directory back towards root, or up to parent of current working directory



cp  

Copies file, needs filename and then place it's moving so cp this.file this.place/
--to copy multiple, list all the files cp 1 2 3 4 destination

--To use a 'wildcard' and select all files in a working directory, use cp * directoryname to move those file theres

--to get all files starting with a letter, do cp m*.txt directoryname to move those files there



mv

Moves files one place to another, same syntax as cp, mv this.file this.place/

--again, can use it for multiple files

--must be in the file where the file is, or reference the full path address of the file, to move it

--CAN ALSO RENAME files, so mv oldfile.name new.name



rm

Removes files

--rmdir removes an empty directory

--rm -r removes the directory and all its child directories, 'r' stands for 'recursive'

--rm –rf does the same removing directories, ignoring nonexistent files, the 'f' is for 'force' and will silently ignore warnings in doing so





touch

Creates a file without content
--also lets you modify the last edited time of an existing file



cat

Creates a file with content
--or lists the contents of a file in the terminal



echo

Accepts a standard input (stdin) which is information inputted into the terminal through a keyboard or other input device, and returns a standard output (stdout), which is that information after a process is run. Standard error (stderr) is an error message output by a failed process.



>

Redirects the stout of the left over to the file on the right. It overwrites the original contents of the file on the right ie: cat file1 > file2



>>

Appends or adds to existing content of a file with new input ie cat newfile >> existingfile or echo "This" >> text.txt



<

Takes the standard input on from file on the right and inputs it into the program on the left, ie cat < text.txt would outputs the text.txt in the terminal



|

Pipe, it takes the standard output of the command on the left and popes it as standard input to the command on the right. This is a command to command redirection. Can be used multiple times to create a pipe from one input, through to a final destination, like a chain reaction



wc

Word count outputs number of lines, numbers, and characters in a file



sort

Takes standard input and orders it alphabetically for a standard output



uniq

Lists only the unique elements in a file, an effective way to do this is to sort and then pipe the file into a new uniq-file, as shown below



Note: you can chain these commands together

Ex: sort file.txt | uniq > uniq-file.txt



grep

'global regular expression point' searches files for a pattern match so grep FindThisPhrase inThisFile.txt

--grep –i makes it case insensitive

--grep –R phrase location searches all files in a directory and –R stands for 'recursive' so it searches for all in a directory and outputs all filenames and lines
--grep –Rl phrase location searches all in a director and outputs only filenames  that match, -l stands for files with matches



sed

'stream editor' it accepts a standard input and modifies it based on an expression, before displaying it as output data, similar to find and replace.  

-sed 's/snow/rain/g' forests.txt
s stands for substitution

snow is the search string, text to find

rain is the replacement string to add in place of snow

g makes it global, so does all instances

Just / means it will just search

^ carat will search beginning of a line

/^b/ will search a line for line that starts with 'b'

$ searches and of line



~

Represents the user's home directory



.

Indicates a hidden file



~/.bash_profile

Is where the environment settings for bash lives, look up for zsh



For Nano:



Ctl O

Ctl X

Ctl G

O = save file, push enter for file name
x = exit

G = help



alias

Command allows you to create word shortcuts (new word to type for pwd, for example, like pd) for commonly used commands ex: alias pd="pwd"



Source ~/.addrxess

Makes the changes in that address come into effect



Export  

Sets command in the profile that sets a variable and exports it, so export PS1="newthing" makes the command prompt look like "newthing" instead of $, export USER="Username" sets username



/bin/

Bin is a directory of scripts for things like pwd, or ls, so you can say /bin/pwd and it's the same as pwd, but you can create your own scripts to use like this



$PATH

Shows list of directories that contains scripts



env

Environment command, displays environment variables for the current user



env | grep PATH

Command that displays the value of a single environment variable. Env is piped to the grep command, which searches the value of the variable PATH and outputs it to the terminal, use this to output the value of any environment variable



less

Like cat, but better for larger files, as it displays content one page at a time, press q to quit

You can configure the less command in the profile, if you export $LESS="-N" it will add line numbers to the file



SCRIPTS

Any command that can be run in the terminal can be run using a script.

Variables are assigned with  an equals sign and no space var="this"

Variables are accessed using a dollar sign

Input arguments can be passed into a bash after the script name, separated by spaces myScript.sh "one" "Two"

Inputs can be requested using the read keyword

Aliases can be created in the .bashrc or .bash_profile using alias thisAlias='file.sh argument'

Scripts have a .sh ending
start the file with a #!/bin/bash on its own line

^the above tells the compute which type of interpreter to use for the script

Store scripts in the ~/bin/ directory

The scripts need "execute" permission to be allowed to run, so always do the terminal command chmod +x scriptName.sh

In the config file  (linux ~/.bashrc, mac ~/.bash_profile) make sure to add the PATH=~/bin:$PATH so that the scripts in ~/bin/ are available and can be run from anywhere by typing the filename like ./scriptName.sh

Set variables by doing varNam="thisThing" no spaces

Reference vars by echo $varNam

If statements in scripts: if [condition] then action else action fi

Comparison operators:

Equal –eq

Not equal –ne

Less than or equal to –le

Less than –lt

Greater than or equal –ge

Greater than –gt

Is null –z

Best practice is to put variables being compared in quotes, to prevent errors if the variable is null or contains spaces

Equal ==

Not equal !=

If ["$foo" == "$bar"]

Loops are  

for word in $paragraph
do  
    echo $word

done

while [ $index –lt 5 ]  

do

echo $index

index=$((index + 1))

done

until [ $index –eq 5 ]

do

echo $index

index $((index+1))

done

Arithmetic in bash scripting uses $((…)) syntax and the variable name  

Use read to ask the user for input and save it to a variable  

read number

Asks user for input and saves it to 'number' variable

Or use scriptname variable1 variable2 to use arguments, which get used as $1, $2 (1 indexed) within the script function

for color in "$@"  

do

echo $color

Done

(the $@ means it will accept an indefinite number of input arguments, or use $1 or $2 for input 1 or 2)

You can also access external files in script;

files=/some/directory/*  

( the * means all files in that directory)

for file in $files

do

echo $file

done

first_greeting="Nice to meet you!"

later_greeting="How are you?"

greeting_occasion=0

echo "How many times should I greet?"

read greeting_limit




while [ $greeting_occasion -lt $greeting_limit ]

do

if [ $greeting_occasion -lt 1 ]

then

echo $first_greeting

else

echo $later_greeting

fi

greeting_occasion=$((greeting_occasion + 1))



fzf

https://github.com/junegunn/fzf

Helps see git diffs, run fzf without parameters it will show list of files in current directory, and typing will filter the list

Generate  

It can display the results of a command, so bat (which is a command like cat but supports syntax highlighting)

Use fd to run



bat

https://github.com/sharkdp/bat

Prettier cat, but has line numbers so to copy use bat main.cpp | xclip  



delta

https://github.com/dandavison/delta





head

Reads the first few lines of any text given as an input and writes them as a standard output (which, by default, displays it on the screen)

http://www.linfo.org/head.html

Defaults to displaying first 10 lines

Head filename filenames  

Head –n15 filename   //displays 15 lines

Head –c5 filename //displays 5 bytes which includes  newline characters

Head –c5k filename //displays 5 kilobytes

Head –n3   //no filename, just spits back the last 3 lines written into the keyboard



tail

Same as head but for last lines of a program



read

Can be used to split a string into an array using –a

read –a bar <<< $foo

Takes a string, foo, and splits it into an array, bar. The array index can be accessed through:

${foo[index]}



xargs

Runs next command input after it xarg git add //runs git add, useful with pipery
