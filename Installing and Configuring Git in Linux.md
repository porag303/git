## Install Git on Linux

To install Git on a Linux system (Debian/Ubuntu-based distros), use the following command:

`sudo apt install git`

>This will install the Git version control system.

## Configure Git UserName and Email

Before you start using Git, it’s essential to set up your user information so commits can be properly attributed to you.

Set Global UserName and Email:

```
git config --global user.name "Porag"
git config --global user.email "porag303@gmail.com"
```
>The `--global` flag ensures that these settings apply to all repositories on the system. If you want to set different credentials for specific repositories, you can use `--local` instead.

## Check Git UserName and Email

To verify the settings you’ve applied:

`git config --list`

This will list all the configurations (user name, email, etc.). If you only want to check the user name or email individually:

```
git config user.name
git config user.email
```

## Unset/Remove UserName or Email

If you ever want to remove or change the user name or email, you can use the following commands:

```
git config --global --unset user.name
git config --global --unset user.email
```

>After unsetting, you can reconfigure them again with the `git config` commands as mentioned in Step 2.

## Check Configuration Files

Git stores configuration files in different locations:

    -Global Configuration: ~/.gitconfig (or /home/username/.gitconfig)
    -Local Configuration: .git/config within each repository.

To check the configuration files, you can navigate to the home directory and inspect the `.gitconfig` file:

```
cd /home
ls -a
```
Then you can open the .gitconfig file with any text editor:

`open .gitconfig`

## Generate SSH Key for GitHub/Remote Repositories

SSH keys are often used for secure authentication with remote repositories (e.g., GitHub, GitLab). You can generate an SSH key using:

`ssh-keygen -o -t rsa -C "porag303@gmail.com"`

This will create an SSH key pair (public and private) in the default location (~/.ssh/).

    `-o`: Ensures the use of OpenSSH's new format for the private key.
    `-t rsa`: Specifies the RSA encryption algorithm.
    `C`: Provides a comment to help identify the key (usually your email).

Once you’ve generated the SSH key, you’ll need to add the public key (`~/.ssh/id_rsa.pub`) to your GitHub (or other platform) account.

## Git Stages Overview

Git has a staged workflow consisting of the following stages:
<ol><li><b>Working Directory:</b> This is where you make your changes. Files here are untracked or modified versions of files that are tracked by Git.</li>
<li><b>Staging Area (Index):</b> Once you are ready to commit changes, you add files to the staging area. This is like preparing files to be included in your next commit.</li>
<br>

_Example:_

```
git add <filename>  # Stages specific file
git add .           # Stages all modified and new files
```
<li><b>Local Repository:</b> This is where your commits are stored on your machine. After staging, you commit your changes here.</li>
<br>

_Example:_

`git commit -m "Commit message"  # Commits staged changes to the local repo`

<li><b>Remote Repository:</b> This is a version of the repository hosted on a platform like GitHub, GitLab, or Bitbucket. You push your local commits to this remote repository to share with others or back up your work.</li>
<br>

_Example:_

`git push origin main  # Pushes commits to the 'main' branch of the remote repository` </ol>
