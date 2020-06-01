# Welcome to SRCT!

Student-Run Computing and Technology (SRCT, pronounced "circuit") is a student organization at George Mason University which enhances student computing at our school by developing and maintaining systems that provide specific services for Mason's community. We were founded in 2011 to be a place where students could work together, share their knowledge, and build really neat projects for the benefit of everyone at Mason, as well as run a host of events to help get students involved.

Whether you're looking to contribute to one of our web projects or just find a group of people who love technology to hang out with, there's lots of ways be involved in SRCT.

## Slack

Regardless of how you plan to participate, you need to join the SRCT Slack! Slack is an online communication platform, and we use it for everything. On Slack, we plan our meetings, plan meetups, work on our projects, and just chat. Signup for an account using your GMU email address at https://srct.slack.com/signup, then once you're in, say hi!

## Getting involved

### Meetings

A great first step into SRCT is to attend our meetings. We host weekly meetings on Monday's at 6pm where we invite guest speakers, run techincal workshops, play board games, or just hang out and work on our projects. Check our website calendar at https://srct.gmu.edu to see when the next meeting is.

### Planning

Lots of work goes into planning our meetings and events. If you want to make an impact on the org but aren't interested in contributing to our technical projects, helping to plan events is a great way to do that! To start, hang out at our meetings or post in Slack that you're interested and we'll get you involved.

## Projects

The main focus of our org is building software to benefit the Mason community. Hopefully you've used some of our software already, such as [Schedules](https://schedules.gmu.edu), [What's Open](https://whatsopen.gmu.du), or [Go](https://go.gmu.edu). We're always looking to add new features, improve existing features, and fix bugs in our software, so new contributors are always welcome. To get started contributing, please follow our inital setup guides for your operating system:

- [Windows](https://github.com/srct/welcome/blob/master/initial-setup-windows.md)
- [Mac](https://github.com/srct/welcome/blob/master/initial-setup-mac.md)
- [Linux](https://github.com/srct/welcome/blob/master/initial-setup-linux.md)

Once you've gotten setup, there's a few crucial technologies you need to be familiar with before you can start contributing.

### Command Line

When working on any kind of software project, you're going to need to navigate around, run commands, and get yourself out of trouble on the command line. Learning the basics will take you far. If you're already familiar, feel free to skip ahead. If not, please complete the [DjangoGirls Introduction to command line](https://tutorial.djangogirls.org/en/intro_to_command_line/). This will get you up to speed with the basics.

**NOTE**: if you're on Windows, use Git Bash to complete the tutorial and follow the OSX/Linux instructions. You'll use Git Bash to contribute to our projects so it's best to learn that instead of the default windows interface.

## Git Workflow

Git is the industry standard for version control, and it's what we use to manage our projects. Git is a necessary skill for software developement as it allows you to collaberate efficiently and effictively with other developers while building software.

To understand how Git is used in our projects, follow the following tutorial to add your name to our [Contributor Page](https://srct.github.io/welcome/).

**Make sure you've followed the initial setup instructions for your operating system!**

## Making Code Changes

Although it may seem intimidating at first, updating the code behind SRCT's projects is a very routine process. However, it does take some getting used to. This guide is here to walk you through your first technical contribution. Feel free to use it as a reference at any time!

<!--
### Prerequisites

// Feel free to add anything here about what needs to be installed prior, such as ssh keys

-->
### Cloning

The first step that must be taken prior to contributing to any project is cloning a copy of it to your own computer. With the copy, you can make any adjustments that you'd like without affecting the original stored on GitHub. To do this, go to the GitHub page of whichever project you're interested in. For us, that will be [github.com/srct/welcome](https://github.com/srct/welcome). Once here, click the bright green *Clone or download* button. In the pop-up window, ensure that *"Clone with SSH"* is displayed. If not, click *Use SSH*. From here, copy the information in the text box. For us, it should be: *git@github.com:srct/welcome.git*. Now, in your command line, head to a folder where you'd like all of your SRCT projects to be kept. Then, clone the project using: `git clone git@github.com:srct/welcome.git`.

Run `cd welcome` to navigate into the project directory.

### Branching

Now that you have the project stored on your computer, you're going to create a new "branch." When on this branch, you can add, remove, and edit the projects files. However, doing so will leave the project unchanged on the original branch, "master". To create a new branch and move to it, use `git checkout -b <branch name>`. Feel free to name the branch whatever you'd like!

There are now three versions of the project. One, stored on GitHub, is the official production version. A second, stored on your computer, is contained in the branch "master" and is up-to-date with the version on GitHub. A third, also stored on your computer, is contained in the new branch that you've just created. Since no changes have been made to it, it is currently identical to the other two. Let's change that!


## Adding Your Name

Contained in the project, there should be a file by the name of "index.html". Open that using whatever web browser you'd prefer to get a look at it. Currently, a list of names should be displayed. However, it's missing a name: yours!

Open the "index.html" with whatever text editor you feel comfortable with (*ie. Sublime Text, NotePad++, Visual Studio Code, etc...*). If you've never seen an HTML file before, don't sweat it! It simply displays the contents of webpages using a series of nested "tags". Inside of the `<ul>` tag, there should be at least one series of `<li><h3> {{ Name }}  </li></h3>` tags. This is what is displaying all of the current names. To add yours, replicate that code underneath of the last, inserting your name.

Now, if you open the `index.html` file, you should see your name on the page!

### Commit your changes

Now that you've added your name, it's time to save, or *commit* the change. To do this, you first need to *add* the file to tell Git you want your changes to this file to be saved:

    git add index.html

Now, we can use the `git commit` command to save your changes.

    git commit -m "<message>"

Feel free to set the meessage to whatever you'd like.

### Push the branch

With your change to `index.html` saved on your branch, the next step is to upload the branch with your change to the GitHub project. This way, the project manager will be able to review your changes to make sure everything is correct, and suggest feedback if it is not.

Do this by running

    git push

Oops! Before you can push to a SRCT GitHub project, you need to be added to the group. In Slack, post a message in the #help channel with your GitHub username asking to be added to the group and we'll add you as soon as we can.

Once you've been added to the group, run `git push` again. Another error should appear. Before you can push, Git needs to know *where* to push to. Run the suggested command to tell Git to push to our GitHub page.

### Merging your changes

With your branch on GitHub, it's time to formally ask for your changes to be merged into the projects `master` branch. Once this happens, the changes will be reflected on the live webpage. This process of asking for permission is called a "pull request". Go to the [Welcome GitHub page](https://github.com/srct/welcome) and create a new pull request from your branch.

Your pull request will then be reviewed by a project manager and merged into the `master` branch if everything looks good. Once it's merged, head to https://srct.github.io/welcome/ to see your hard work!










<!-- - Just hang out!
    - Learn from tech talks, meetings
    - No pressure
    - Game nights
    - Dinners, #friendfinder
    - Marketing
- Contributor
    - Basic command line stuff (https://tutorial.djangogirls.org/en/intro_to_command_line/)
    - Git tutorial
        - PRINT https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf
    - Add your name to contributor site
        - Pretty SRCT Logo plus list of names, just html file
    - Look at our projects, pick one that looks interesting
    - Post in slack
    - Look at the open issues, ask about them in slack -->
