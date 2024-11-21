# Git

Welcome to the **Git Wiki**! This is your go-to resource for learning and mastering Git, the powerful version control system used by developers worldwide to collaborate and manage code efficiently.  

## Description  

Git is a distributed version control system that allows developers to track changes in their code, collaborate with others, and maintain the integrity of their projects. It’s widely adopted in open-source projects, professional development workflows, and personal coding projects.  

This wiki covers the basics of Git, its commands, workflow tips, and practical examples to get you started.  

## Useful Links  

- [Official Git Documentation](https://git-scm.com/doc)  
- [GitHub Learning Lab](https://lab.github.com/)  
- [Pro Git Book (Free)](https://git-scm.com/book/en/v2)  
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)  
- [GitHub Git Tutorial](https://docs.github.com/en/get-started/using-git/about-git)  

## Table of Contents  

- [Description](#description)  
- [Useful Links](#useful-links)  
- [Git Versions](#git-versions)  
- [Basic Git Commands](#basic-git-commands)  

## Git Versions  

Here are some key milestones in the evolution of Git:  

- **2005**  
  Git was created by Linus Torvalds to manage the development of the Linux kernel.  

- **Git 1.x (2005-2010)**  
  Introduced the core functionality, including branching and merging.  

- **Git 2.x (2013)**  
  Added performance improvements, better algorithms for merging, and support for large repositories.  

- **Recent Releases**  
  Ongoing updates include security enhancements, new features, and better integration with modern CI/CD pipelines.  

For a detailed history, visit the [Git Release Notes](https://github.com/git/git/tree/master/Documentation/RelNotes).  

## Basic Git Commands  

Here are some common Git commands with examples to help you get started:  

**Initialize a Repository**  
```bash
git init
```

**Clone a Repository**  
```bash
git clone <repository_url>
```

**Check the Status of Your Repository**  
```bash
git status
```

**Add Files to the Staging Area**  
```bash
git add <file_name>
# Or add all changes
git add .
```

**Commit Changes**  
```bash
git commit -m "Commit message describing the changes"
```

**Push Changes to a Remote Repository**  
```bash
git push origin <branch_name>
```

**Pull Changes from a Remote Repository**  
```bash
git pull origin <branch_name>
```

**Create a New Branch**  
```bash
git branch <new_branch_name>
```

**Switch to a Branch**  
```bash
git checkout <branch_name>
```

**Merge Branches**  
```bash
git merge <branch_name>
```

**View Commit History**  
```bash
git log
```

**Undo Changes**  
```bash
git reset --soft HEAD~1  # Undo the last commit, keep changes staged
git reset --hard         # Undo the last commit and discard changes
```
