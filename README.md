# Version Control in Git/Github for Gahlmann Lab

### A walkthrough of how to use Git/Github together

# Background

We will be doing all of our commands and pushes in the command line. There are GUI tools available but you will eventually run into a situation that you need the command line tools to do. 

First, a little background.

**Git** - Git is a version control software installed on your local machine

**Github** - Github is a for-profit company now owned by Microsoft. Github offers web based hosting for software and code repositories.

**Distributed Version Control** - Git is a distributed version control system. This means that there is not one master copy of the repository. Every developer who checks out the repository has a complete record of the project including all changes to the code. 

**Repository (repo)** - the basic unit in git. This is a record of all changes to specified files in your project.

**Fork** - personal copy of another user's repository

**Branch** - a parallel version of a repository. The top level branch of a repository is not called 'main', formerly called 'master'. 

# Setup

You must be set up with git/github before you are able to use them. 

### Mac/Linux users
Git comes with your operating system. No installation required.

### PC users
Need to install git and git bash. Watch the first 2:45 of this video: [https://www.youtube.com/watch?v=albr1o7Z1nw](https://www.youtube.com/watch?v=albr1o7Z1nw)

### Create GitHub account
Create a free account here: https://github.com/

# Scenario 1: Git Basics

Let's walk through a basic scenario where you have just installed git and github and are using it for the first time

#### Git configuration
Check your git version
```
git --version
```

Set up your config variables
```
git config --global user.name "Your name"
git config --global user.email "Your email"
```

### Clone existing Github repository
This is in the situation that you will be working from an existing Github repository. If you are just starting a new project, I recommend creating an empty repository first in Github.

```
git clone <url> <where to clone (optional)>

ex:
git clone https://github.com/epurpur/gahlmann-lab-version-control
```
This will clone (download) all files, code, change logs, etc for this project onto your project 

Navigate into the new directory
```
cd gahlmann-lab-version-control
```

View information about the remote repository. This can be useful especially in the situation that you have a local project you are working on and want to make sure it has been correctly connected to a github repository.
```
git remote -v
```

### Committing changes locally
Now that we have cloned a repository, we want to develop our code and make changes to it.

First, check the status of our repository
```
git status
```
We havent made any changes so the working tree should be clean. 

Now let's make some changes to the testcode.py file 

***to do this, open testcode.py in any text editor and make some changes to the code. It doesn't matter what changes are made***

Now, let's stage these commits **locally**. Let's see that these are being tracked by git now.
```
git status
```

Add these changes to the staging area

```
git add -A
```

Check the status again

```
git status
```

You see that these changes are ready to be committed

Now, let's commit these changes. Againk we are committing these changes **locally**

```
git commit -m "my message here"
```

Check status again to see that the working tree is clean

```
git status
```

### Committing changes remotely

Remember, the changes we have made are only in effect locally. Now we want to push these changes to our **remote** repository, which in this case is Github.

We are working on the main branch of this repository. We will cover branching in the next scenario.
```
git push origin main

or 

git push
```




