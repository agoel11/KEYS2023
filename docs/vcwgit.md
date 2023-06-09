#Version Control with Git

###Links

[Software Carpentry Version Control with Git Tutorial](https://swcarpentry.github.io/git-novice/)                                                                                                              
[Shell & Git Basics CyVerse](https://foss.cyverse.org/00_basics/)                                                                       
[Git Commands Sheet](https://drive.google.com/file/d/1K3F4_GCemJsxVjGLadyMtOtTTt3jpuVG/view?usp=sharing)

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
`$ git config --global core.editor "nano -w"`
8. The `git init` command will make the directory into a repository that can include subdirectories and their files. Creating a directory and initializing it with Git are two seperate things.
9. We can use the `git status` command at any time to see the status of our repository.
10. Git doesn't automatically keep track of files. Use the `git add` command, followed by the file name, in order to have Git keep track of a file and save changes. You can then use the `git commit` command in order to save everything you have saved through `git add` permanently. A commit message should also be written in order to make describe changes made to the file(s).
11. When updating a file, you can use `git diff` to see the changes made between the last version and the current version. In order to see differences between older commits, simply type `$ git diff HEAD~1 mars.txt`, the number after the tilde (`~`) represents how many commits back you are seeing. Then use `git add` to save the file, and `git commit` to save the version. You can also use `git log` to see a history of changes.
12. Files can be stored in a project’s working directory (which users see), the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).
![image](https://github.com/agoel11/KEYS2023/assets/81878922/7170f30a-1b11-48e7-8a94-30791da428c3)
13. `git checkout` can restore old versions of the file. By typing `$ git checkout HEAD mars.txt` you can restore the last commit, to go back further you wwould need the commit identifier in place of `HEAD`. Remember that we must use the commit number that identifies the state of the repository before the change we’re trying to undo. A common mistake is to use the number of the commit in which we made the change we’re trying to discard. In the example below, we want to retrieve the state from before the most recent commit (HEAD~1), which is commit f22b25e.
![image](https://github.com/agoel11/KEYS2023/assets/81878922/234e00f3-452d-403b-9654-84f42379a9a8)
14. Here is an overall working of Git and Version Control.
![image](https://github.com/agoel11/KEYS2023/assets/81878922/3e6aa511-0698-4890-a9d7-6551f9caa09a)
15. You can also have Git ignore files to save disk space and memory and keep your repository clean. We do this by creating a file in the root directory of our project called `.gitignore`. Then you can add the names of the files, or types of files, as well as the directory they are in, that you want Git to ignore. You must still add and commit the `.gitignore` file however.
16. In order to connect our local files to the cloud, we need a Github repository. The repository should be empty with a README and license. We can connect our local and GitHub repositories by making the GitHub repository a remote for the local repository. Make the GitHub repository SSH, copy its URL, and run this command `$ git remote add origin git@github.com:vlad/planets.git` to connect them.
17. In order to authenticate with GitHub, we can use an SSH. SSH  uses a key pair, a public key and a private key that both must be used. Check what SSH pairs already exist on your machine by using this command `ls -al ~/.ssh`. To create a key pair, use this command, `$ ssh-keygen -t ed25519 -C "iam@ironman.snap"`.
18. Use this command, `cat ~/.ssh/id_ed25519.pub` to copy your public key, and then go to GitHub.com, click on your profile icon in the top right corner to get the drop-down menu. Click “Settings,” then on the settings page, click “SSH and GPG keys,” on the left side “Account settings” menu. Click the “New SSH key” button on the right side. Now, you can add the title, paste your SSH key into the field, and click the “Add SSH key” to complete the setup. Then run the command `$ ssh -T git@github.com` to check the SSH authentication.
19. Once a connection is established, you can use the command `$ git push origin main` to push all your changes to the GitHub repository. You can also pull changes from the GitHub repository by using the command `$ git pull origin main`. This is what our Git system looks like now.
![image](https://github.com/agoel11/KEYS2023/assets/81878922/f1c670c4-45bc-430c-8bd8-0e83da3c8a1b)
