# Covering-BASH-Shell-Tracks

## !!! DISCLAIMER - THIS PROJECT IS NOT INTENDED TO BE USED IN A BAD WAY AND IS INTENDED ONLY FOR EDUCATIONAL PURPOSES I NEITHER CONDONE NOR TAKE RESPONSIBILITY FOR SOMEONE ELSE'S ACTIONS !!!

First of all everyone interested in this topic should know where previously used commands are stored in Linux.

1. If you open up a terminal and type

     - more ~/.bash_history
       - [Lists the content of the bash_history file, which is used to store used commands]

2. Clearing the history of the current BASH Shell

     - history -c
       - [Clears the command history of the selected BASH Shell not for all shells nor for all previously used commands]

       - [After that we need to write the changes to the disk with the same history command just switching the flag to -w]
     - history -w 

3. Disabling the history of BASH Shells

     - export HISTSIZE=0
       - [This command changes the environment variable HISTSIZE to 0. The HISTSIZE variable is the variable that determines how many commands are stored, the default number on your machine would probably be 500 or 1000. You can type in whatever number you want if you want a different number of commands to be stored.]

4. Completely erasing the command history 

     - cat /dev/null > ~.bash_history
       - [With this command we write /dev/null to the bash_history file, which results in the file being blank at the end]
     - history -c
       - [Of course at the end we want EVERYTHING to be erased so we delete the last command too with the -c flag]

5. Shredding the command history

     - shred ~/.bash_history
       - [This command makes the entire history transform into unreadable binary data]
       
     - shred ~/.bash_history && cat /dev/null > .bash_history && history -c  
       - [If you want to take a step further you can combine the shred command and then writing /dev/null to the bash_history file to completely erase the evidence of any activity]

That wraps up my quick tutorial on anti-forensics in a BASH Shell thank you for reading it and I hope you find it helpful!

By nodlezgucci!
