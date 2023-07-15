---
title: "GIT for Beginners"
seoTitle: "Git Basics"
seoDescription: "Git is a widely-used and free open-source version control system that helps developers manage and keep track of different versions of their software project"
datePublished: Tue Feb 07 2023 21:22:39 GMT+0000 (Coordinated Universal Time)
cuid: cldur067d00010amehbek6s8k
slug: git
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/wX2L8L-fGeA/upload/8342a088c2907a6290d54d8427c47b90.jpeg
tags: github, javascript, development, git, devops

---

Git is a distributed version control system that allows developers and operations teams to collaborate and keep track of the changes made on a project. GIT as a DevOps tool empowers collaboration and faster release cycles.

Git has two repository types local and remote.

The local repository is on the local machine and the remote is on the central server. We can always pull/push our code/data on remote/local repositories as well and others can also make changes to the code/data.

In Local Repository, data will be passed to the staging area and then commit files. The working area is the untraced state.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ada2660d-24fd-445a-a7a8-5f711c472dc3/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230207%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230207T093847Z&X-Amz-Expires=86400&X-Amz-Signature=9910351f4dfc576c593be221dc1a39d4d90ae9104e0e7040efcfcd65f99b2dee&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

### What is GitHub?

GitHub is a web-based platform that provides hosting for software development projects that use the Git version control system. It allows developers to store, manage and track changes to their code over time, collaborate with others on projects and contribute to open-source projects.

### **Differences between git and GitHub:**

1. Git is a version control system, while GitHub is a web-based hosting platform for Git repositories.
    
2. Git allows you to manage and keep track of your source code history locally, while GitHub provides a remote, collaborative environment.
    
3. Git commands are executed in the terminal, while GitHub offers a graphical user interface to interact with Git repositories.
    
4. Git is free and open-source, while GitHub offers both free and paid plans for individuals and organizations.
    
5. Git enables collaboration through remote repository cloning and merging, while GitHub provides additional collaboration features such as pull requests, issues, and project boards.
    

### GIT installation

We can simply install git using this link to any of the platforms and by following the steps:

[https://git-scm.com/downloads](https://git-scm.com/downloads)

I have installed it using home-brew, please find the below commands for the same.

```bash
brew install git: To install git 
git --version: to check the current version of git
```

### Git repository:

A Git repository is a virtual storage area where you can save versions of your code. It is used to track changes in your source code over time and collaborate with other developers by sharing your code and contributing to others' code. The repository contains all the files, branches, and history of changes that have been made to the code.

![Git Tutorials - Git Commands - DevOps Courses and Certification](https://www.devopsuniversity.org/wp-content/uploads/2021/01/git-repository.jpg align="left")

### Git Init:

The git init command is the first command that you will run on Git. The git init command is used to create a new blank repository. It is used to make an existing project a Git project. Several Git commands run inside the repository, but the init command can be run outside of the repository.

```bash
#git init : It is used to initialising git
```

### Git Add:

The git add command is used to add file contents to the [Index (Staging Area)](https://www.javatpoint.com/git-index). This command updates the current content of the working tree to the staging area. It also prepares the staged content for the next commit. Every time we add or update any file in our project, it is required to forward updates to the staging area.

```bash
#git add <file_name>: It is used to put data in staging area
```

### Git Status:

The git status command is used to display the state of the repository and staging area. It allows us to see the tracked, untracked files and changes. This command will not show any commit records or information.

Mostly, it is used to display the state between [**Git Add**](https://www.javatpoint.com/git-add) and **Git commit commands**. We can check whether the changes and files are tracked or not.

```bash
#git status: To check the status of data , after git add it should be in staging area
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675801004375/397e0d33-7091-4893-9276-fb87c730cc72.png align="center")

At times, we have to let it know who is making the changes in git to make a record of the changes.

```bash
#git config [user.name](http://user.name) “aman”

#git config [user.email](http://user.email) “aman@example.com”
```

Here is a few more useful commands :

```bash
#git restore “file.txt” : It will store the previous version of file. 

#git commit -m “updated text” : It will update the create a new story and saves the new copy of the story, this way we can avoid going to the text editor and updating it. 

#git add . : with this command we can stage more than one file in staging area 

#git log: To get the log details 

#git log --name-only: Detailed logs with file names 

#git log -n 1 : latest commit in the new repository.
```

### **GIT Braches:**

In Git, branches are separate copies of a project that can be worked on independently. It is used to avoid mistakes in the master branch and separately we can run the code through git and test it.

They allow multiple team members to work on different features or bug fixes simultaneously without interfering with each other. Branches have their own set of commits and changes made on one branch do not affect the others. Developers can create pull requests to merge changes from one branch to another. The main branch is called "master" and is considered stable. Git flow is a branching model that helps Organise and track work in a structured way for large projects.

```bash
#git branch “branch_name” : Create a new branch 

#git checkout “branch_name”: switch to an existing branch

#git checkout -b “branch_name”: create a new branch and switch to it 

#git branch -d “branch_name: To delete the branch ‘d stands for delete’

#git branch: List all the branches 

#git branch -a: Lists all branches in the local and remote repository.

# git merge “branch_name”: 1. Merges the specified branch into the current branch. ( It can be done through master branch)
```

Note: fast-forward merge: It can happen when the current branch has no extra commits compared to the branch which we are merging.

```bash
#git pull "remote" "branch_name": Fetches the specified branch from the remote repository and merges it into the current branch.

# git branch -D "branch_name": Force deletes the specified branch.

#git branch -m "old_branch" "new_branch": Renames the specified branch.

#git stash: Stashes changes in the working directory, allowing you to switch branches without committing changes.

#git stash apply: Applies the changes stashed in the last stash command.
```

**Head:** It is the current location in the repository, it will move automatically whenever we switch branches.

As you can see the HEAD always points to the last commit on the currently checked-out branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675801866767/38f48c42-c3fe-4f31-81af-9fa5d8906f3b.png align="center")

### Git Remote:

In Git, the term remote is concerned with the remote repository. It is a shared repository that all team members use to exchange their changes. A remote repository is stored on code hosting services like an internal server, GitHub, Subversion, and more.

```bash
git remote: The given command is providing the remote name as the origin. Origin is the default name for the remote server, which is given by Git.
git remote -v: The above output is providing available remote connections. If a repository contains more than one remote connection, this command will list them all.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675803338775/a243a9a8-5a8a-4280-953d-97abdceee6a2.png align="center")

### Git Push, pull & clone:

The **git push** command is used to upload local commits to a remote repository. The syntax for the command is as follows:

```bash
git push [remote-name] [branch-name]
```

Where remote-name is the name of the remote repository, and branch-name is the name of the branch that you want to push to the remote repository. This command is typically used after making local changes and committing them to your local repository, to share those changes with others who are collaborating on the project.

**git pull** is a command used in Git to retrieve new changes from a remote repository and merge them into the current branch. It is a combination of ***git fetch*** and ***git merge*** commands and is typically used to synchronize a local repository with a remote one.

```bash
git pull <remote> <branch>
```

where &lt;remote&gt; is the name of the remote repository and &lt;branch&gt; is the name of the branch you want to pull changes from.

**git clone:** The git clone command is used to create a copy of a remote repository on a local machine.

```bash
git clone [remote-repository-url]
```

Where remote-repository-url is the URL of the remote repository that you want to clone. This command creates a new directory with the same name as the remote repository and copies all of the files and their history into the new directory. This is useful for creating local copies of remote repositories for development or collaboration.

### Git Fetch and Merge:

**Git Fetch:** Git Fetch is a command used in Git to retrieve new changes from a remote repository and bring them into the local repository. It is typically used to synchronize a local repository with a remote one. The command retrieves the changes but does not merge them into the local repository, allowing the user to review the changes before merging them. The command is used in the following format:

```bash
git fetch <remote> <branch>
```

where &lt;remote. is the name of the remote repository and &lt;branch&gt; is the name of the branch you want to fetch the changes from. If no branch is specified, git fetch retrieves changes from all branches of the remote repository.

Git Merge: git merge is a command used in Git to combine changes from multiple branches into the current branch. It is typically used to bring changes from a remote branch into the local branch that you are currently working on.

```bash
git merge <branch>
```

where &lt;branch&gt; is the name of the branch you want to merge into the current branch.

For Ex: If we have two commit messages from two different users we can correct them (Incase of wrong msgs) and commit the changes with new changes.

### Fork:

A fork in Git is simply a copy of an existing repository in which the new owner disconnects the codebase from previous committers. A fork often occurs when a developer becomes dissatisfied or disillusioned with the direction of a project and wants to detach their work from that of the original project.

A `git fork` is a feature of Git and Github that allows users to create a separate copy of a repository under their own account. This allows users to make changes to the code and propose changes to the original repository.

On the other hand, `git clone` is a command used to copy an existing Git repository from a remote server to a local computer. `git clone` creates a local copy of the entire repository, including all branches, commits, and history. The cloned repository is linked to the original repository, so changes can be easily synced between the two.

In summary, `git fork` is a feature of Git and Github that enables users to create a separate copy of a repository, while `git clone` is a Git command used to create a local copy of a remote repository. The main difference is that `git fork` creates a separate copy under a different account, while `git clone` creates a local copy of the entire repository.

### **Git rebase:**

**Git rebase** is a command used to reapply commits from one branch on top of another branch. The \*\*`git rebase`\*\*command is used to perform this operation. The main use of rebasing is to clean up a feature branch by removing unnecessary merge commits and making a linear history, making it easier to understand and maintain the branch.

```bash
git rebase master
```

In general, \*\*`git merge`\*\*is a safer option for integrating changes in a collaborative environment, as it preserves the history of both branches and makes it clear when and how changes were integrated. On the other hand, \*\*`git rebase`\*\*can be useful for cleaning up a branch's history and avoiding multiple merge commits, but it should only be used in a non-collaborative environment or with caution in a collaborative one.

### **git cherry-pick:**

\*\*`git cherry-pick`\*\*is a Git command that allows you to select and apply specific commits from one branch onto another branch. This can be useful when you want to apply specific changes from a branch without merging the entire branch into yours.

```bash
git cherry-pick <hash of the commit >
```

### **Git Revert and Reset:**

**Git Revert:** Used to revert the commit already done, it is used to undo changes and keep those changes in the git history . Below are two general commands that we use, there are a few more commands.

```bash
git revert <commit-ish>: The commit option is used to revert a commit. To revert a commit, we need the commit reference id. The git log command can access it.
git revert -e <commit-ish>: It is used to edit the commit message before reverting the commit. ( -e stands for edit)
```

**Git Reset:** "git reset" is a Git command that is used to reset the state of your Git repository to a specific commit or a specific state. The reset command can be used to unstaged changes, to unmodified files, or to reset the branch pointer to a different commit.

There are three main options for `git reset;--mixed`, `--soft`, and `--hard`. The default option is `--mixed`, which resets the branch pointer to the specified commit, but keeps the changes in the working directory and index, allowing you to review and recommit the changes if desired.

```bash
git reset [commit]: Resetting the branch pointer to a specific commit:
git reset: This command unstages changes, leaving them in the working directory.
git reset [file]: This command unmodifies the specified file, leaving it in the working directory.
git reset --hard [commit]: This command resets the branch and index to the specified commit, discarding all changes in the working directory.
```

Here is a picture that will help you to understand more:

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d314c312-226c-48a9-a8ca-b25d62004177/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230225%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230225T152951Z&X-Amz-Expires=86400&X-Amz-Signature=c4dcc9e0463cf00a2ddc8903862e9f56891d541a71dcd933f324ac0a162c290e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

### **Stashing**:

"Stashing" in Git is a way to temporarily save changes that have not yet been committed to a branch. This allows you to switch to a different branch, perform some other work, and then later come back and apply the stashed changes. The stash is stored as a "stack" of changes, so you can have multiple stashes and choose which one to apply later.

```bash
git stash : To save the changes 
git stash save "<Stashing Message>" : We can save the changes with a message
git stash list: It gives the list of all stash changes with stash@{} ID. 
git stash apply: command is used to reapply changes that were previously stashed using git stash. This allows you to switch back to a branch you were working on, apply the stashed changes, and continue your work.
git stash apply <stash id>: It will save the changes to the stage were you want. 
git stash show: This command will show the file that is stashed and changes made on them.
git stash show -p: -p stands for the partial stash. The given command will show the edited files and content.
git stash pop: It is a Git command that combines the functionality of both git stash apply and git stash drop. It reapplies the changes from the most recent stash, and then removes the stash from the stash list.
git stash drop: This command is used to delete a stash from the queue. Generally, it deletes the most recent stash.
git stash drop <stash id>: To delete a particular stash from the queue.
git stash clearL: This command allows deleting all the available stashes at once.
git stash branch <Branch Name>: This command will create a new branch and transfer the stashed work on that.
```

### **Git Reflog:**

"git reflog" is a Git command that provides a log of changes to the state of your Git repository, including branch references and HEAD. The reflog is stored in the `.git/logs/` directory and is a record of all changes to the branches and HEAD in your repository, including branch updates, resets, and other operations.

The reflog is useful in a variety of situations, including:

1. Recovering lost commits: If you have lost a commit or made a mistake during a reset or rebase operation, you can use the reflog to find the commit and recover it.
    
2. Debugging repository state: If you are unsure of the state of your repository, you can use the reflog to see all the changes that have been made, and how they have affected the branches and HEAD.
    
3. Undoing operations: If you have made a mistake or want to undo an operation, you can use the reflog to find the state of the repository before the operation and reset the repository to that state.
    

```bash
git reflog: Gives all the alternation done previously. Its shows all the changes in the repo

git reset --hard [commit-reference-in-reflog]: The git reflog command is an essential tool for Git users, as it provides a way to recover from mistakes and track changes to the state of the repository. It is recommended that you regularly run git reflog to keep track of changes to your repository and to ensure that you have a way to recover from mistakes.
```

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9cf5e4d2-147d-4931-9b8a-2b14f8cd38a4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230207%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230207T211838Z&X-Amz-Expires=86400&X-Amz-Signature=011020a7d1270caea826c5164dfc57edafbd3e5b3df3940e960da339d9460f75&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

GIT Object Contents:

1. Commit: It's is simply a commit
    
2. Tree: It is a folder on out File system, associated with a repository.
    
3. blob: It is just a piece of data.
    

NOTE: All the commits are saved in ./.git/objects folder.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b61a5e7d-3c41-4463-a68c-1406841ca88c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230209%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230209T075526Z&X-Amz-Expires=86400&X-Amz-Signature=29f3006489be85dd866a9931dc3c5ace41a0c63d797c29cf06ab135540a49b4e&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b61a5e7d-3c41-4463-a68c-1406841ca88c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20230207%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20230207T211926Z&X-Amz-Expires=86400&X-Amz-Signature=16572310534eda825146969fdf9b866a9a9d1caae8b12f555b6f22e0bf031f3b&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%22Untitled.png%22&x-id=GetObject align="left")

Thank you !!

#Kodekloud

#[www**.kodekloud.com**](http://www.kodekloud.com)