# Test

A public repository for testing, and learning the in's and out's of Git

## Timeline

### 23/05/2013 Log #1:
Will begin learning git using the git documentation 

> http://git-scm.com/documentation

### 28/06/2013 Log #2:
Starting from Chapter 2: Git Basics

**Learned Basic Git Workflow**

- ```git status```
- ```git add <filename>```
- ```git commit -v -a -m "commit message"```
	- used after the files are staged, and this command commits it onto the brach. ```-v``` is used to add the git diff log. ```-a``` skips the git add command and allows for immediate commit. ```-m``` to add the commit message for self-identification 
	- ```git commit --amend```
		- used to undo a commit
- ```git diff```
	- used to give an indepth log of changed lines of each file from last commit
- ```git rm -f```
	- used to remove a file from the staging area, using the ```-f``` to **forcifully remove a non-tracking file** in order to prevent accidental removal of untracked files
- ```git mv file_from file_to```
	- used to rename, or move files in git
	- a much simpler solution than the conventional linux ```mv```
- ```git checkout -- <filename>```
	- a dangerous command, because git can recover all commited files, but non-commited files will be lost

**Git files**

- .gitignore

**Git History**

- ```git log -p -2```
	- brings out the commit log, ```-p``` brings out the diff log along, and ```-number``` shows the most recent number of entries
	- [useful formating tools for log](git-scm.com/book/en/Git-Basics-Viewing-the-Commit-History)

**Remote Git**

- ```git remote -v```
	- gives a list of remote handles, ```-v``` gives the URL list
- ```git remote add [shorname] [url]

