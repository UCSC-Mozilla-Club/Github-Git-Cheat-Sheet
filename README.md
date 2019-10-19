## **GitHub Git Cheat Sheet**

Git is an open source distributed version control system that facilitates GitHub activities on your laptop or desktop. Git cheat sheet guide to enhance your workflow. This cheat sheet saves you time when you just can't remember what a command is or don't want to use git help in the command line. It is hard to memorize all the important Git commands by heart, so save it to your desktop to resort to when you get stuck. There included the basic Git commands to learn Git, and more advanced concepts around Git branches, remote repositories, undoing changes, and more.


## **Catalog**

 - **[Install Git](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#install-git)**
 - **[How to use Git](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#how-to-use-git)**
 - **[Configure tooling](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#configure-tooling)**
 - **[Create repositories](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#create-repositories)**
 - **[Make changes](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#make-changes)**
 - **[Group changes](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#group-changes)**
 - **[Refactor filenames](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#refactor-filenames)**
 - **[Suppress tracking](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#suppress-tracking)**
 - **[Save fragments](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#save-fragments)**
 - **[Review history](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#review-history)**
 - **[Redo commits](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#redo-commits)**
 - **[Synchronize changes](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#synchronize-changes)**
 
##  [**INSTALL GIT**](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#install-git)
GitHub provides desktop clients that include a graphical user interface for the most common repository actions and an automatically updating command the line edition of Git for advanced scenarios.


### [For Windows users](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#for-windows-users)


1. Download the executable Git file from [git-scm.com/downloads](https://git-scm.com/downloads)  
2. Run the installation file with Administrator rights  
3. Choose an appropriate installation location such as C:\_tools\git  
4. Install the default components, including Git GUI Here and Git Bash Here  
5. Choose your preferred Git default editor. [We recommend Notepad++.](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-set-Notepad-as-the-default-Git-editor-for-commits-instead-of-Vim)  
6. Allow Git to be added to the Windows PATH  
7. Accept the default line ending conversion for Unix and Windows compatibility  
8. Chose the extra option to enable system caching  
9. Click Finish to complete the install.  
10. Choose to open a Git Bash shell and start using Git!

![enter image description here](https://itknowledgeexchange.techtarget.com/coffee-talk/files/2019/03/how-to-install-git-on-windows.gif)

### [**For macOS users**](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#for-macos-users)
There are two main ways to install Git on Mac.


***Option 1 :***
The easiest way to install Git is to install the Xcode Command Line Tools which comes with Git among other things. On Mavericks (10.9) or above you can do this simply by trying to run the git command from the Terminal.

 1. Open a Terminal on your Mac. Now, type the following command into your Terminal.

    `$ git --version`
     
 2. If you don’t have git installed already, it will prompt you to install it.

![enter image description here](https://hackernoon.com/hn-images/1*qv5WfS6PbPf1xUT4eJFIDA.gif)

 3. Read and agree to the Command Line Tools License Agreement and you are ready to use Git!

***Option 2 :***

 1. Download Git https://git-scm.com/download/mac
 
 ![enter image description here](https://hackernoon.com/hn-images/1*Arrf9mdXO_0baPX6VO1tpQ.gif)

2. Once your download is finished, open the file and go through the installation process.

![enter image description here](https://hackernoon.com/hn-images/1*qZ8cyEmJ7PK_r3q0KByl3Q.png)

3. Done !

![enter image description here](https://hackernoon.com/hn-images/1*9NiX3v9blBAnlccxUazuLA.png)

### [**For Linux users**](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#for-linux-users)
***Installing Git with Default Packages***
Ubuntu’s default repositories provide you with a fast method to install Git. Note that the version you install via these repositories may be older than the newest version currently available.

1. First, use the apt package management tools to update your local package index. With the update complete, you can download and install Git

     `$ sudo apt update`
     `$ sudo apt install git`

2. You can confirm that you have installed Git correctly by running the following command

    `$ git --version`

***Installing Git from Source***
A more flexible method of installing Git is to compile the software from source. This takes longer and will not be maintained through your package manager, but it will allow you to download the latest release and will give you some control over the options you include if you wish to customize.

1. You need to install the software that Git depends on. This is all available in the default repositories, so we can update our local package index and then install the packages.

   ` $ sudo apt update`
    `$ sudo apt install make libssl-dev libghc-zlib-dev libcurl4-gnutls-dev libexpat1-dev gettext unzip`

2. After you have installed the necessary dependencies, you can go ahead and get the version of Git you want by visiting the [Git project’s mirror on GitHub](https://github.com/git/git)

3. From here, be sure that you are on the `master` branch. Click on the **Tags** link and select your desired Git version. Unless you have a reason for downloading a _release candidate_ (marked as **rc**) version, try to avoid these as they may be unstable.

![enter image description here](https://assets.digitalocean.com/articles/git_install_1604/branch-tags.png)

4. Next, on the right side of the page, click on the **Clone or download** button, then right-click on **Download ZIP** and copy the link address that ends in `.zip`.

![enter image description here](https://assets.digitalocean.com/articles/git_install_1604/download-zip.png)

5. Back on your Ubuntu 16.04 server, move into the `tmp` directory to download temporary files.

    `$ cd /tmp`

6. From there, you can use the  `wget`  command to install the copied zip file link. We’ll specify a new name for the file:  `git.zip`.

    `wget https://github.com/git/git/archive/v2.18.0.zip -O git.zip`

7. Unzip the file that you downloaded and move into the resulting directory by typing:

    `$ unzip git.zip`
    `$cd git-*`

8. Now, you can make the package and install it by typing these two commands:

    `$ make prefix=/usr/local all`
    `$ sudo make prefix=/usr/local install`

9. To ensure that the install was successful, you can type  `git --version`  and you should receive relevant output that specifies the current installed version of Git.

10. Now that you have Git installed, if you want to upgrade to a later version, you can clone the repository, and then build and install. To find the URL to use for the clone operation, navigate to the branch or tag that you want on the  [project’s GitHub page](https://github.com/git/git)  and then copy the clone URL on the right side:

![git copy URL](https://assets.digitalocean.com/articles/git_install_1604/copy-url.png)

11. At the time of writing, the relevant URL is https://github.com/git/git.git

12. Change to your home directory, and use  `git clone`  on the URL you just copied:

    `$ cd ~`
    `$ git clone https://github.com/git/git.git`

This will create a new directory within your current directory where you can rebuild the package and reinstall the newer version, just like you did above. This will overwrite your older version with the new version

##  **[HOW TO USE GIT](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#how-to-use-git)**

**Windows**  
Right click on any location and click  `git bash`.

**Linux and Mac**  
Open  `Terminal`  to use git.

##  [**CONFIGURE TOOLING**](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#configure-tooling)

You can specify Git configuration settings with the ***git config*** command. One of the first things you did was set up your name and email address.
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
## [**CREATE REPOSITORIES**](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#create-repositories)

Say you’ve got an existing project that you want to start tracking with git.

-   Go into the directory containing the project.
-   Type  `git init`.
-   Type  `git add`  to add all of the relevant files.
-   You’ll probably want to create a  `.gitignore`  file right away, to indicate all of the files you don’t want to track. Use  `git add .gitignore`, too.
-   Type  `git commit`.

You’ve now got a local git repository. You can use git locally, like that, if you want. But if you want the thing to have a home on github, do the following.

-   Go to  [github](https://github.com/).
-   Log in to your account.
-   Click the  ***new repository*** button in the top-right. You’ll have an option there to initialize the repository with a ***README*** file.
-   Click the ***Create repository*** button.

Now, follow the second set of instructions, “Push an existing repository…”
```
$ git remote add origin git@github.com:username/new_repo
$ git push -u origin master
```
Actually, the first line of the instructions will say
```
$ git remote add origin https://github.com/username/new_repo
```
## **[MAKE CHANGES](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#make-changes)**

Review edits and craft a commit transaction  

 - `$ git status  `

Lists all new or modified files to be committed  

 - `$ git diff`

Shows file differences not yet staged  

 - `$ git add [file ]`

Snapshots the file in preparation for versioning  

 - `$ git commit -m “[descriptive message “]`

Records file snapshots permanently in version history

 - `$ git commit -m "[descriptive message]"`

## **[GROUP CHANGES](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#group-changes)**

List all local branches in the current repository

 - `$ git branch`

Creating a branch for your work

 - If you have collaborator permissions on a repository, you can create
   a branch off of the repository's default branch so you can safely
   experiment with changes.
 - `$ git branch [branch-name]`
 
Switching between branches
 - You can view and make commits to any of your repository's branches.
 - `$ git checkout [branch-name]`

Committing and reviewing changes to your project

GitHub Desktop tracks all changes to all files as you edit them. You can decide how to group the changes to create meaningful commits.

Reverting a commit

 - You can revert a commit to undo the last saved work on your branch.

Viewing the branch history

 - When you click a commit on the  **History**  tab, you can see more
   details about the commit, including a diff of the changes the commit
   introduced.
 - `$ git merge [branch-name]`

Delete the specified branch

 - `$ git branch -d [branch-name]`

## **[REFACTOR FILENAMES](%28https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#refactor-filenames)**

If you added a file in an earlier commit, you need to remove it from your repository history. You can remove files from your repository history using either the BFG Repo-Cleaner or the  `git filter-branch`  command. 

If the file was added with your most recent commit, and you have not pushed to GitHub, you can delete the file and amend the commit:

1.  Open  Git Bash.
    
2.  Change the current working directory to your local repository.
    
3.  To remove the file, enter  `git rm --cached`
    ```
    $ git rm --cached [file]
    ```
4.  Commit this change using  `--amend -CHEAD`:    
    ```
    $ git commit --amend -CHEAD
    # Amend the previous commit with your change
    # Simply making a new commit won't work, as you need
    # to remove the file from the unpushed history as well
    ```
5.  Push your commits to GitHub:
    ```
    $ git push
    # Push our rewritten, smaller commit
    ```

**[SUPPRESS TRACKING](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#suppress-tracking)**
**Exclude temporary files and paths**
 Lists all ignored files in this project
***.log 
build/
 temp-***
 
  A text file named .gitignore suppresses accidental versioning of files and paths matching the specified patterns.
  
 **$ git ls-files --other --ignored --exclude-standard** 

**[Save fragments](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#save-fragments)**

**Shelve and restore incomplete changes**
Temporarily stores all modified tracked files
**$ git stash** 

Lists all stashed changesets
 **$ git stash list**
  
 Restores the most recently stashed files 
  **$ git stash pop** 
  
  Discards the most recently stashed changeset.
  **$ git stash drop**
   
   
  **[Review history](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#review-history)**
  
 **Browse and inspect the evolution of project files**

Lists version history for the current branch 
  **$ git log**
  
Lists version history for a file, including renames
   **$ git log --follow [file]** 
   
Shows content differences between two branches 
    **$ git diff [first-branch]...[second-branch]** 
   
Outputs metadata and content changes of the specified commit 
    **$ git show [commit]** 
   
 **[Redo commits](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#redo-commits)**

**Erase mistakes and craf replacement history** 

Undoes all commits after [commit], preserving changes locally
**$ git reset [commit]** 

 Discards all history and changes back to the specified commit
 **$ git reset --hard [commit]** 

 
 **[Synchronize changes](https://github.com/UCSC-Mozilla-Club/Github-Git-Cheat-Sheet#synchronize-changes)**

**Register a repository bookmark and exchange version history**

Downloads all history from the repository bookmark
 **$ git fetch [bookmark]** 
 
  Combines bookmark’s branch into current local branch 
  **$ git merge [bookmark]/[branch]** 
 
 Uploads all local branch commits to GitHub
  **$ git push [alias] [branch]** 
  
  Downloads bookmark history and incorporates changes
   **$ git pull** 
   








 

