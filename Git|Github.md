

# 📋Note:
	
	The purpose of further researching this tool is to learn and apply it in my personal and professional projects. The notes I’ve taken are key points I consider important and useful for future reference.

# 🔗Referencias:

	I’ve used the MoureDev YouTube channel as a reference because of its clear explanations and solid experience in software development. Feel free to follow the channel:
	
	https://youtu.be/3GymExBkKjE?si=DMHTAkJNLqJ44Ued
	

## What is GIT - GITHUB


### GIT

	- Version control
    
	- Open source
    
	- Distributed

### GITHUB

	Code hosting platform

## Resources:

	https://git-scm.com/
	
	https://git-scm.com/book/en/v2
	
	https://github.com/
	
	https://training.github.com/downloads/github-git-cheat-sheet/
	
	https://docs.github.com/en

## Context:	

	https://es.wikipedia.org/wiki/Git
	
## Instalation of git hub

	https://git-scm.com/downloads


# Let's go

## Version

	git --version

## Help

	git -h

## Comands 

	ls
		list all directories 
	
	cd
		move to another folder
	
	cd ..
		go back to previous folder
	
	pwd
		show current location
	
	mkdir "nombre"
		create a new folder
	
	code.
		open Visual Studio Code

## Configuracion de GIT

	Associate user name and email:
		
	git config --global user.name "nombre"
	git config --global user.mail "grulla@mail.com"

## GIT INIT
	
	touch prog.py
	git init
		initialize Git in the current folder

	Customize terminal: [Oh My Zsh](http://ohmyz.sh)

## Git Branches

	git branch -m main
		rename the main branch

## Git ADD y COMMIT

	git status
		check project status
		
	git add hellogit.py
		track file with git 
		
	git commit -m "Commit sobre..."
		commit with message
		
## GIT LOG y STATUS

	git log
		check commit history 

## GIT CHECKOUT Y RESET

	git checkout hellogit2.py
		return to specific file version
	
	git reset
		reset to last snapshot
	
	git log --graph
		visual branch graph
	
	git log --graph --pretty=oneline 
		one line
	
	git log -- grapgh --decorate --all --oneline
		decorate

## GIT ALIAS

	git config --global alias.tree "log -- grapgh --decorate --all --oneline"
		git tree

## GITGNORE

	touch .gitignore
	
		**/.name
			Add ignored files or folders:

## GIT DIFF

	git diff
		see changes made

## Checkout

	To move through the different states

	git checkout "hash"
		to locate yourself in that state with the hash
	git checkout "PROYECTO.PY"	
		
	git checkout HEAD
		to indicate which state you want to work in

## GIT RESET HARD Y REFLOG

	git reset --hard
		discard changes, but with hard it is more
	git reflog
		complete interaction history

## GIT TAG

	To tag important references
	
	git tag project_1
		how to name that point
		
	git add .
		add everything pending
	
	git tag
		to see list of tags
	
	git checkout tags/tag
		to move with tags
	
	git checkout main

## GIT Branch y Switch

	git branch nombre
		to create a branch

	git switch nombre
		to move to the branch you want to work on

## Git Merge

	To combine the changes
	git merge main
		merge the data into our branch

## Conflicts en GIT

	When several teams modify the same code in the code editor, what has been modified is observed and what corresponds is left.

## GIT STASH

	Temporarily store uncommitted work:
	
	git stash
		save work  
		
	git stash list
		list stashed changes
		
	git stash pop
		apply lates stash
		
	git stash drop
		delete a stash

## Git Reintegration

When a feature is completed and needs to be merged into the main branch:

1-Check for differences and conflicts:
	git diff rama1

2-Merge
	git merge rama1

3-Check status
	git status
	

## Delete Branches

	git branch -d branch_name
		
## Introduction to GitHUb

## Website:

	https://github.com/


## Getting started

	https://docs.github.com/es
	
### Create account and explore platform.
	
## Local y remote

	Sync local projects with GitHub.
	
## SSH Authentication

	https://docs.github.com/en/authentication

For windows:

[Generating a new SSH key and adding it to the ssh-agent - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```powershell
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```

## Create a Project Repository

New repository creation.

## Git Remote

	git remote add origin https://github.com/Gru11a/git-github1.git

	git push -u origin main

## Push Project

## Git Fetch y Pull

### fetch

	download history only  

### git pull 

	download history and changes
		

## Git Clone

	git clone git@github.com:Gru11a/git-github1.git
		clone project locally
	
## Git Push

	upload changes to GitHub

## GitHub fork

	Copy someone else’s project to your own repository.

## ## Collaborative Flow

	Work on a forked project and contribute back to the original.

	Remember to **Sync fork** to verify synchronization.

## Pull Request

To contribute to the original repository:

1. Click **Contribute** and send a pull request.
    
2. The original project owner will review and accept/reject it.
    
3. Once accepted, apply changes with **Merge pull request**.

## Graphical tools

### Gitkracken
	
	Great for open-source projects.
	
### Sourcetree
	
	Ideal for private repositories.

### Git-fork

	Another alternative GUI.

## Git & GitHub Flow

Workflows

https://www.gitkraken.com/learn/git/git-flow
https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow

## Git Cherry-Pick Y Rebase

### Cherry Pick
	
	Bring a specific commit into the current branch:

	git cherry-pick hash
	git cherry-pick --i
	git cherry-pick --continue
	git cherry-pick --abort
### Rebase

	Apply a branch to a specific point, rewriting commit history:

	git rebase 	--i
	git rebase 	--continue
	git rebase 	--abort

## GitHub Pages & Actions

To publish websites:
	https://pages.github.com/

For automation workflows:
	https://github.com/features/actions

		
