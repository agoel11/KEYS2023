#Version Control with Git

###Links

[Software Carpentry Version Control with Git Tutorial](https://swcarpentry.github.io/git-novice/)                                                                                                 
[Shell & Git Basics CyVerse](https://foss.cyverse.org/00_basics/)

###Notes

1. Nothing that is committed to version control is ever lost. All old versions of files are saved, so it’s always possible to go back in time to see exactly who wrote what on a particular day, or what version of a program was used to generate a particular set of results. Because of that we know who to ask if we have questions later on, and, if needed, revert to a previous version, much like the “undo” feature in an editor. The version control system automatically notifies users whenever there’s a conflict between one person’s work and another’s (editing and overwriting).
2. Version control is the lab notebook of the digital world: it’s what professionals use to keep track of what they’ve done and to collaborate with other people. Every large software development project relies on it, and most programmers use it for their small jobs as well.
3. Version Control with Git is used in the UNIX Shell and run in the same way, just with different commands.
4. Version control systems start with a base version of the document and then record changes you make each step of the way.
5. A version control system is a tool that keeps track of changes for us, effectively creating different versions of our files. It allows us to decide which changes will be made to the next version (each record of these changes is called a commit), and keeps useful metadata about them. The complete history of commits for a particular project and their metadata make up a repository. Repositories can be kept in sync across different computers, facilitating collaboration among different people.
6. On a command line, Git commands are written as `git verb options`, where `verb` is what we actually want to do and `options` is additional optional information which may be needed for the `verb`. Here is an example of how to first configure Git.
```
$ git config --global user.name "Tony Stark"
$ git config --global user.email "iam@ironman.snap"
```
This is the same username and email as your GitHub account and will be used to publish your changes directly to Github.
7. You must also set the default text editor you want to use. Here is an example of that command for the `Nano` editor.                                                                                      
`	$ git config --global core.editor "nano -w"`
