# SRCT Initial Setup - Windows

In order to contribute to SRCT projects, you need to install some software for both running the projects and editing code.

# GitHub account

If you haven't already, sign up for a GitHub account at https://github.com.

### SSH Keys

To interact with GitHub, you need to upload your SSH keys. This lets GitHub identify who you are when you try to download and push changes to projects. Please follow the instructions on [this page](https://github.com/srct/welcome/blob/master/ssh-keys.md) to setup your SSH Keys.

# Software

These packages are used in every SRCT project.

### 1. Install Chocolatey

For Windows, we recommend using Chocolatey for installing software. It allows you to install almost all the software you need with just one command, instead of managing dozens of manual installers.

Start powershell as an administrator, then run

    Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

Curious what this does? Read more on the [Chocolatey Docs](https://chocolatey.org/install).

Next, close PowerShell and reopen it again (also as an administrator).

### 2. Install Git

Git is the software we use for version control.

    choco install git

Next, search for and open as administrator the "Git Bash" program. Use this now instead of PowerShell.

Please note: after you install a program with Chocolatey, you need to **restart your Git Bash** in order for the installation to take effect.

### 3. Install Slack

Slack is what we use to communicate.

    choco install slack

After slack is installed, sign up for an account using your GMU email at https://srct.slack.com/signup.
Log in using this account to the app you just installed. If any of these steps break, post in the #help channel!

### 4. Install VSCode

VSCode is a text editor that we recommend for editing code. It includes built in git integration, along with a powerful plugin system. Plus, it's pretty. If you have another preferred editor, feel free to use that instead. (No, Microsoft Word is not a text editor, and please don't use Notepad!)

    choco install vscode

### 5. Install JavaScript

First, install node.js. Node allows you to run JavaScript programs on your computer.

    choco install nodejs

Next, install Yarn, which is used for installing JavaScript packages used in our applications.

    choco install yarn

### 6. Install MySQL

MySQL is the database of choice for SRCT projects.

    choco install mysql

We need to configure the root user and add a password. Open cmd.exe as an administrator and run the command

    mysql -u root -p

then hit enter again to login.

In the MySQL shell, run the following command:

    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';

Now type `exit` to exit the MySQL shell. This command set the root password to `root` and made this user compatible with the database software our projects use.
