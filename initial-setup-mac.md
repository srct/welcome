# SRCT Initial Setup - Mac

In order to contribute to SRCT projects, you need to install some software for both running the projects and editing code.

# GitHub account

If you haven't already, sign up for a GitHub account at https://github.com.

### 1. SSH Keys

To interact with GitHub, you need to upload your SSH keys. This lets GitHub identify who you are when you try to download and push changes to projects. Please follow the instructions on [this page](https://github.com/srct/welcome/blob/master/ssh-keys.md) to setup your SSH Keys.

# Software

These packages are used in every SRCT project.

### 2. Install Homebrew

For Mac, we recommend using Homebrew for installing software. It allows you to install almost all the software you need with just one command, instead of managing dozens of manual installers.

Launch `terminal.app`, then run

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

After Homebrew installs, run

    brew tap caskroom/cask

This allows you to install applications along with just developer tools.

### 3. Install developer tools

Run the following command to install a variety of necessary developer tools for Mac:

    xcode-select --install

### 4. Install Slack

Slack is what we use to communicate.

    brew cask install slack

After slack is installed, sign up for an account using your GMU email at https://srct.slack.com/signup.
Log in using this account to the app you just installed. If any of these steps break, post in the #help channel!

### 5. Install VSCode

VSCode is a text editor that we recommend for editing code. It includes built in git integration, along with a powerful plugin system. Plus, it's pretty. If you have another preferred editor, feel free to use that instead. (No, Microsoft Word is not a text editor, and please don't use Notepad!)

    brew cask install visual-studio-code

### 6. Install JavaScript

First, install node.js. Node allows you to run JavaScript programs on your computer.

    brew install node

Next, install Yarn, which is used for installing JavaScript packages used in our applications.

    brew install yarn

### 7. (Optional) Install MySQL

**Only necessary if you are working on Schedules, Go, or What's Open.**

MySQL is the database of choice for SRCT projects.

    brew install mysql

Run the command `mysql.server start` to start the database server, and if you want to stop it, run `mysql.server stop`.

We need to configure the root user and add a password. Start the database server then run the command

    mysql -u root -p

then type `root` and hit enter again to login.

In the MySQL shell, run the following command:

    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';

Now type `exit` to exit the MySQL shell. This command set the root password to `root` and made this user compatible with the database software our projects use.
