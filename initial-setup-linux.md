# SRCT Initial Setup - Linux

In order to contribute to SRCT projects, you need to install some software for both running the projects and editing code.

# GitHub account

If you haven't already, sign up for a GitHub account at https://github.com.

### 1. SSH Keys

To interact with GitHub, you need to upload your SSH keys. This lets GitHub identify who you are when you try to download and push changes to projects. Please follow the instructions on [this page](https://github.com/srct/welcome/blob/master/ssh-keys.md) to setup your SSH Keys.

# Software

These packages are used in every SRCT project.

### 2. Install Git

For Linux, most of the necessary program installations can be handled by your distro's package manager, so using the terminal will suffice.
For Debian, Ubuntu, Linux Mint, and most other Linux distros, `apt` is used for installing apps. Since this is more common, it will be used throughout this tutorial.
If you use Red Hat, CentOS, or Fedora, then you can generally just replace `apt` with `yum` or  `dnf`.

Git is the software we use for version control.

    sudo apt update
    sudo apt install git

### 3. Install Slack

Slack is what we use to communicate.

    sudo apt install slack

After slack is installed, sign up for an account using your GMU email at https://srct.slack.com/signup.
Log in using this account to the app you just installed. If any of these steps break, post in the #help channel!

### 4. Install VSCode

VSCode is a text editor that we recommend for editing code. It includes built in git integration, along with a powerful plugin system. Plus, it's pretty. If you have another preferred editor, feel free to use that instead. (No, Microsoft Word is not a text editor, and please don't use Notepad!)

    sudo apt install visual-studio-code

### 5. Install Snap

Snap is a software deployment and package management system that will be needed in the next step to install node.js.

    sudo apt install snapd

### 6. Install JavaScript

First, install node.js. Node allows you to run JavaScript programs on your computer.

    sudo snap install node --classic --channel=12

Next, install Yarn, which is used for installing JavaScript packages used in our applications.

    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
    sudo apt install yarn

### 7. (Optional) Install MySQL

**Only necessary if you are working on Schedules, Go, or What's Open.**

MySQL is the database of choice for SRCT projects.

    sudo apt install mysql-server
    sudo apt install libmysqlclient-dev

Run the command `sudo service mysql start` to start the database server, and if you want to stop it, run `sudo service mysql stop`.

We need to configure the root user and add a password. Start the database server then run the command

    sudo mysql -u root -p

then hit enter again to login.

In the MySQL shell, run the following command:

    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';

Now type `exit` to exit the MySQL shell. This command set the root password to `root` and made this user compatible with the database software our projects use.
