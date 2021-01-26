[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Revisions and the Cloud**

## Important Concepts

* Git is a dvcs(distributed version control system) which allows you to easily collaborate and manage code in a remote repository.
* Github is an online place to store your code(in the cloud) using Git.
* Git helps with version tracking, reviewing changes and keeping changes separate until you want to add them.
* Version control is a system that allows you to store various versions of files as you change them.
* Storing various versions allows you to revert changes and to manage collaborative changes to a file or project.

### Useful Git Commands

* clone - create a copy of an existing repository 
  * > $ git clone https://github.com/test mydirectory 
* status - check the status of a file
  * > $ git status
* add - track files in a repository and stage for commit
  * > $ git add filename  
  * > $ git add * 
* commit - committing changes saves a version or snapshot of file 
  * > $ git commit -m "made changes"
  * > $ git commit -a
* push - pushes your changes to a remote repository (specific branch)
  * > $ git push origin master 
* stash - temporarily removes changes and gives you a clean working branch
  * > $ git stash
  * > $ git stash apply 
  
  
#### Extra Resources

* *View a comprehensive Git tutorial [here](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#2).*
