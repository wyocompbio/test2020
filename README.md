---
title: Introduction to Git 
date: June 02, 2020
author: Vikram E. Chhatre
---




## Table of Contents


[1. What is Git and Why do I need it?](#what-is-git-and-why-do-i-need-it)

[2. How does Git work?](#how-does-git-work)





## 1. What is Git and Why do I need it?


Git is a version control system.  Don't let that make you feel like you are a software engineer.  You don't have to be one for it to be useful to you.  In the simplest terms, git keeps a journal of all the changes you will make to any files and folders (create, edit, copy, move, delete etc.) in a given project.  Think of it as a virtual assistant that is always listening and keeping track of what you do.  

GitHub as you probably already figured out, is an online resource that allows people to host and archive their code.  The code can be updated/maintained from multiple computers that you may have access to.  You may keep it all to yourself, share it with collaborators or if its useful enough, share it with the community at large.  Code is divided into repositories on GitHub and you may have one or a hundred each dedicated to a different project you are working on.  Consider that you are teaching a course for which you may host the weekly materials such as presentations, assignments and exam solutions to a GitHub repository and then share the repo with your students.  

As you can see, one doesn't really need to be a software programmer for Git and GitHub to be useful to them.  With this introduction, we are barely scratching the surface.  In the Further Reading section below, you will find additional resources to learn about these tools. For now, we will set up your environment so it's usable today.




## 2. How does Git work?



- **Note For Windows Users**: Please install git from [here](https://gitforwindows.org)

- Open the commandline terminal on your system.  For Windows, right click and choose Git Bash.  For Mac, search for terminal in the spotlight search.

<center>
<img src="git-bash.png" width=300></img>
<img src="terminal.png" width=400></img>
</center>




- Check whether git is working on your system:

```bash

git --version

git version 2.20.1 (Apple Git-117)

```
   

- To check git's documentation i.e. help manual


```bash

man git

```

<center>
<img src="githelp.png" width=750></img>

</center>


- To exit the interactive documentation

```bash
q

```



- Check the Status of the current directory where your prompt is located:


```bash

git status

fatal: not a git repository (or any of the parent directories): .git

```


- You haven't created any git repositories yet on your system, so this warning message is to be expected.

- Let's create a new repository for testing purposes. First, check where you are on the system, then create a new folder named gitproject.


```bash

pwd

/Users/wyoibc

mkdir gitproject

cd gitproject

pwd

/Users/wyoibc/gitproject

```



- Initiate a new repository

```

git init

Initialized empty Git repository in /Users/wyoibc/gitproject/.git/

```


- Check the status again

```bash

git status

On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

```

- This is normal as well since we haven't yet created any content in here.  Now let's go ahead and create a new file.


```bash

touch README.md

vim README.md

```

- Create some content in the file


```bash
---
title: Learning the Basics of Git
author: Wyoming IBC
date: October 7, 2019
---

This is a new repository.

```

- Save the changes and exit

```bash

:wq

```

- Now check the git status again


```bash

git status


On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

nothing added to commit but untracked files present (use "git add" to track)

```

As you can see, Git is now aware of the changes you made to this repository.  It knows that there is a new file, although the file is not yet on Git's roll call.  This is by design.  Often times, you don't want every file/folder to be tracked by git.  So git only tracks changes in files when you ask it to.  Let's go ahead and do that.


```bash

git add README.md

git status

On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   README.md

```

