#UNIX Shell

###Links

[Software Carpentry UNIX Shell Tutorial](https://swcarpentry.github.io/shell-novice/index.html)

[Shell & Git Basics CyVerse](https://foss.cyverse.org/00_basics/)

[UNIX Shell Commands](https://drive.google.com/file/d/1LcvPbvkkYcssL65ZuwfsRVrzk6GqjB5m/view?usp=sharing)

###Notes

1. The Unix shell is both a command-line interface (CLI) and a scripting language, allowing such repetitive tasks to be done automatically and fast. The shell is a program where users can type commands. With the shell, it’s possible to invoke complicated programs like climate modeling software or simple commands that create an empty directory with only one line of code. The most popular Unix shell is Bash.
2. General Syntax of a Shell Command                                                                                                                                  
![image](https://github.com/agoel11/KEYS2023/assets/81878922/e48a13a1-72ee-43b0-9777-3abb94a5dee0)
3. Shell commands are used to navigate, visualize, modify (files/folders) and automate (processes), and can only be executed through the shell's terminal window.
4. Once something is deleted from the Shell, it is gone forever. There is not recycle bin.
5. The most effective way to use the Shell is to combine commands such as capturing output, filtering output, and passing output in what are known as pipes.  `cut -d, -f 2 animals.csv | sort | uniq -c | wc -l`
6. We can use for loops in order to repeat tasks over many files or instances. Loops can also be nested and can be written in one line or multiple. This is the basic syntax of a for loop.
```
# The word "for" indicated the start of a "For-loop" command
for thing in list_of_things 
#The word "do" indicates the start of job execution list
do 
    # Indentation within the loop is not required, but aids legibility
    operation_using/command $thing 
# The word "done" indicates the end of a loop
done
```
8. You can also use the `echo` command to see what your Shell command would do without actually running it.
9. You can save numerours commands in a file, called a Shell Script, and re-run all those operations by typing a single command. This helps with time management, error prevention, and reproducibility. By adding commands to a file, and then calling that file using the `bash` command, you can execute the script. You can add as many commands as you want in the file. You can also use the `$` command followed by a number to add arguments to the command when calling the script.                                                                                                                                                                                     
For example, this script: `head -n 15 "$1" | tail -n 5`                                                                                                                                                                      
Can be called with this command (note the parameter for the `$1`): `$ bash middle.sh octane.pdb`
10. A very useful command for filtering and finding is the `grep` command. It can be used to find all items in a file that include the key word (passed as a parameter). Things like word boundaries and case can also be limited for different results.
