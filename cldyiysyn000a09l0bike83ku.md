---
title: "Git and GitHub a Mystery"
seoTitle: "Git and GitHub"
datePublished: Fri Feb 10 2023 12:48:43 GMT+0000 (Coordinated Universal Time)
cuid: cldyiysyn000a09l0bike83ku
slug: git-and-github-a-mystery
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1676032872506/7eb7ab59-208a-4d73-9f28-cc52f4c43eef.jpeg
tags: github, git, git-commit, git-basic, coderscommunity

---

Do you want to work on open-source projects? Do you want to develop a project with your friends? then Git is the best thing to learn.

# What is version control?

Version control is a system which records the changes in a file or set of files of a folder and with the help of which we can go back to any version of the file.

For example, you have a task to build an app which has three screens your customer has given you some guidelines to develop the screen now you have developed the first screen and to make it more user friendly you have made some more changes but your customer does not like it hence you need to go back to the previous version now and here version control comes into play.

# What is Git?

It is important to understand Git before learning it. Other version control system considers the data they store to be a collection of files and the modifications made to each file over time whereas Git works in a different way Git effectively takes a photo of how all of your files appear at that precise moment and keeps a reference to that snapshot each time you commit, or save the state of your project.

# Difference between Git and GitHub

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675914063069/24d8a98d-9d7a-4400-ba50-23ec34b5685c.png align="center")

Git is a version control system as discussed above and GitHub is a web hosting platform for version control like any other hosting service like GitLab, Bitbucket etc.

## **Git installation process:**

Git installation is straightforward and you can download it from the [official website](https://git-scm.com/downloads) depending on your Operating System.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675916858124/17e8f7b2-1a55-4135-89d3-48d93f3468e1.png align="center")

To verify the git installation run the command:

```plaintext
 git --version
```

in the command line terminal and you will get the version as output.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675917208727/fa98557c-67a5-418b-af5c-09e27e67a366.png align="center")

# Push code in GitHub:

### Initial Setup:

```plaintext
git config --global user.name "your name"
git config --global user.email your@email.com
```

This is crucial since each Git commit uses it and the commits you start making contain it in an immutable manner. It is done only for the first time as we are using the **\--global** flag.

### Initialize the Git repo:

By using the below command we can initialize an empty git repository.

```plaintext
git init
```

### Staging and committing:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675944266211/14f63a41-a3b5-4661-a8ca-254a0c62633f.png align="center")

Let us understand each stage properly:

1. Untracked stage: This is the first stage where the files are initially present after the initialization of the repository.
    
2. Unmodified: This stage is reached after we make a commit. what is commit? we will understand in few minutes.
    
3. Modified: This stage is reached when we are tracking the files and we have made some changes to it.
    
4. Staged: This is the stage where the files are added for making a commit.
    

Let's start with the first command toward staging:

```plaintext
git add filename
```

Initially, the files are untracked so after running the above command the file will be **tracked** as well as it will be available in the **staging** area. Now if we make some changes in that file then it will go to the **modified** stage.

### Committing the changes:

First, let's understand what is commit? Commit is a snapshot of the changes we have made in a file and we can go back to this version in future.

For committing the changes, the files need to be in the staging area and it can be found by the command:

```plaintext
git status
```

If the files are in the staging area then use the below command to make a commit.

```plaintext
git commit -m "added few changes"
```

### Pushing the code:

Steps to push the code in GitHub:

* We need to add the remote repo link in Git, remote repo means the repo which you have created in GitHub.
    
* Copy the link and then run the below command:
    

```plaintext
git remote add origin link
```

* In the above link by convention, we are writing **origin** which is for our own repo link name and in the place of link pass the link.
    
    Till now if you have made a commit which is to be pushed then run the below command.
    

```plaintext
git push origin master
```

here **origin** is the name of the link and **master** is the branch name.

## Conclusion

Git and GitHub is a very important skill for software developers and Git is a very powerful version control system combinely they help you to showcase your learning, network with people and do open-source contributions hence learning them and spending time on them will be a good decision.