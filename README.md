# Test

A public repository for testing, and learning the in's and out's of Git

## Timeline

### 05/23/2013 Log #1:
Will begin learning git using the git documentation 

> http://git-scm.com/documentation

### 06/28/2013 Log #2:
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
- ```git remote add [shortname] [url]```
	- adding a remote repository
- ```git push [remote-name] [branch-name]```
	- will push it the repository back to the remote for sharing
- ```git remote rename```
	- to rename the remote's shortname
- ```git remote rm [shortname]```
	- to remove the remote 

### 07/16/2013 Log #3:
Continuing Chapter 2: Git Basics

**Tagging**

Useful to tag certain points in history as important. 
- ```git tag -l 'v1.4.2.*'```
	- list tags with starting of v1.4.2
- ```git tag -a v1.4 -m 'my version 1.4'```
	- create an annotated tag
	- replace ```-a``` with ```-s``` to sign tags with GPG
- ```git show v1.4```
	- shows the specific tag data
- ```git push origin --tags
	- push tags onto remote servers for sharing

Chapter 3: Git Branching

- The most important concept utilized in git, allows divergence of different histories of the repository

**Git Branching**

- ```git branch [branch-name]```
	- makes a new branch
- ```git checkout [branch-name]```
	- switches to the branch

**Basic Branching and Merging**

- A basic branching workflow would include ```git checkout -b [branch-name]``` to make and checkout to the new branch
- Then move back to master branch with ```git chekcout master```
- Create another branch with ```git checkout -b [new-branch-name]```
- Merge the [new-branch-name] with [master] by ```git checkout master``` then ```git merge [new-branch-name]``` then ```git branch -d [new-branch-name]``` if its not needed anymore

**Branch Management**

