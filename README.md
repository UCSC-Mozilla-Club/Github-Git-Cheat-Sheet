# Github Git Cheat Sheet

Git  is  the  open  source  distributed  version  control  system  that  facilitates  GitHub  activities  on  your  laptop  or 
desktop. This cheat sheet summarizes commonly used Git command line instructions for quick reference.


## INSTALL GIT

### For windows users

1. Download [Git for Windows Setup](https://git-scm.com/download/win)
2. Install Git through the setup.Usually leave all configurations in default.

### For mac Os X users

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
```bash 
$ yum install git
```
(up to Fedora 21)

 ```bash
$ dnf install git
```
(Fedora 22 and later)

#### Gentoo
```bash
$ emerge --ask --verbose dev-vcs/git
```

#### Arch Linux
```bash
$ pacman -S git
```