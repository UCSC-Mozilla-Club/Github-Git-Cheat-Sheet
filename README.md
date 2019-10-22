## Learn Git and GitHub 

**Git** is a  distributed version-control. Distributed version control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed,  data integrity. Data integrity  and support for distributed, non-linear workflows.


desktop. This cheat sheet will help you with commonly used Git command line instructions for quick reference.



### Catalog


- **[Install Git](#install-git)**

- **[How to use Git](#how-to-use-git)**

- **[Configure tooling](#configure-tooling)**

- **[Create repositories](#create-repositories)**

- **[Make changes](#make-changes)**

- **[Group changes](#group-changes)**

- **[Refactor filenames](#refactor-filenames)**

- **[Suppress tracking](#suppress-tracking)**

- **[Save fragments](#save-fragments)**

- **[Review history](#review-history)**

- **[Redo commits](#redo-commits)**

- **[Synchronize changes](#synchronize-changes)**

## INSTALL GIT

### For Windows users

1. Download [Git for Windows Setup](https://git-scm.com/download/win)


2. Install Git through the setup. Usually all configurations can be left in default settings.


### For macOS users

Download [Git for Mac](https://git-scm.com/download/mac)

### For Linux users
```
#### Debian/Ubuntu

For the latest stable version for your release of Debian/Ubuntu

```bash

$ sudo apt-get update

$ sudo apt-get get install git
```
For Ubuntu, this PPA provides the latest stable upstream Git version

```bash

$ sudo add-apt-repository ppa:git-core/ppa

$ sudo apt update

$ sudo apt install git

```
#### Fedora



For releases up to Fedora 21

```bash 
$ yum install git



```
For Fedora 22 and later

$ dnf install git

#### [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#arch-linux)Arch Linux

$ pacman -S git

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#how-to-use-git)HOW TO USE GIT

**Windows**  
Right click on any location and click  `git bash`.

**Linux and Mac**  
Open  `Terminal`  to use git.

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#configure-tooling)CONFIGURE TOOLING

**Configure user information for all local repositories**  

Set the name you want attached to your commit transactions - $ git config --global user.name "[name]"

Set the email address you want attached to your commit transactions - $ git config --global user.email "[email address]"

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#create-repositories)CREATE REPOSITORIES

**Start a new repository or obtain one from an existing URL**

Create a new local repository with the specified name - $ git init [project-name]

Download a project and its entire version history - $ git clone [url]

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#make-changes)MAKE CHANGES

**Review edits and craft a commit transaction**

List all new or modified files to be commited - $ git status

Show file differences not yet staged - $ git diff

Snapshot a file in preparation for versioning - $ git add [file]

Snapshot all files of the current directory in preparation for versioning - $ git add .

Unstage the file (reset), but preserve its contents - $ git reset [file]

Record file snapshots permanently in version history - $ git commit -m "[descriptive message]"

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#group-changes)GROUP CHANGES

**Name a series of commits and combine completed efforts**

List all local branches in the current repository - $ git branch

Create a new branch - $ git branch [branch-name]

Switch to the specified branch and updates the working directory - $ git checkout [branch-name]

Combine the specified branch's history into the current branch - $ git merge [branch-name]

Delete the specified branch - $ git branch -d [branch-name]

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#refactor-filenames)REFACTOR FILENAMES

**Relocate and remove versioned files**

Delete the file from the working directory and stages the deletion - $ git rm [file]

Remove the file from version control but preserves the file locally - $ git rm --cached [file]

```

Change the file name and prepares it for commit - $ git mv [file-original] [file-renamed]

```

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#suppress-tracking)SUPPRESS TRACKING

**Exclude temporary files and paths**

List all ignored files in this project - $ git ls-files --other --ignored --exclude-standard

```

A text file named .gitignore suppresses accidental versioning of files and paths matching the specified paterns -
 *.log
build/
temp-*

```

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#save-fragments)SAVE FRAGMENTS

**Shelve and restore incomplete changes**

Temporarily store all modified tracked files - $ git stash

```

List all stashed changesets - $ git stash list

```

Restore the most recently stashed files - $ git stash pop

```

Discard the most recently stashed changeset - $ git stash drop

```

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#review-history)REVIEW HISTORY

**Browse and inspect the evolution of project files**

List version history for the current branch - $ git log

```

List version history for a file, including rename - $ git log --follow [file]

```

Show content differences between two branches -  $ git diff [first-branch]...[second-branch]

```

Output metadata and content changes of the specified commit - $ git show [commit]

```

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#redo-commits)REDO COMMITS

**Erase mistakes and craf replacement history**

Undo all commits afer [commit], preserving changes locally  -  $ git reset [commit]

```

Discard all history and changes back to the specified commit - $ git reset --hard [commit]

```

## [](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#synchronize-changes)SYNCHRONIZE CHANGES

**Register a repository bookmark and exchange version history**

Download all history from the repository bookmark - $ git fetch [bookmark]

```

Combine bookmark’s branch into current local branch - $ git merge [bookmark]/[branch]
```
click the following link for more information
[Github Guide](https://guides.github.com)







