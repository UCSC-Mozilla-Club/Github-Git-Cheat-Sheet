# GitHub Git Cheat Sheet

Git  is  the  open  source  distributed  version  control  system  that  facilitates  GitHub  activities  on  your  laptop  or 
desktop. This cheat sheet summarizes commonly used Git command line instructions for quick reference.

### Catalog

- **[Install Git](#install-git)**<br>
- **[How to use Git](#how-to-use-git)**<br>
- **[Configure tooling](#configure-tooling)**<br>
- **[Create repositories](#create-repositories)**<br>

## INSTALL GIT

### For Windows users

1. Download [Git for Windows Setup](https://git-scm.com/download/win)
2. Install Git through the setup. Usually all configurations can be left in default settings.

### For macOS users

Download [Git for Mac](https://git-scm.com/download/mac)

### For Linux users

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
 ```bash
$ dnf install git
```

#### Gentoo

```bash
$ emerge --ask --verbose dev-vcs/git
```

#### Arch Linux

```bash
$ pacman -S git
```

## HOW TO USE GIT

**Windows**<br>

Right click on any location and click `git bash`.

**Linux and Mac**<br>
Open `Terminal` to use git.

## CONFIGURE TOOLING

**Configure user information for all local repositories**<br>

Sets the name you want attached to your commit transactions
```bash
$ git config --global user.name "[name]"
```

Sets the email you want attached to your commit transactions
```bash
$ git config --global user.email "[email address]"
```

## CREATE REPOSITORIES

**Start a new repository or obtain one from an existing URL**

Creates a new local repository with the specified name
```bash
$ git init [project-name]
```

Downloads a project and its entire version history
```bash
$ git clone [url]
```