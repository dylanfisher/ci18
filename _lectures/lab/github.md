---
title:            GitHub
subtitle:         Instructions for creating a GitHub account and repository
lecture_date:     2017-01-24 00:00:00 -0500
section:          Lab
---

### Create a GitHub account and repository

1. Sign up for a [GitHub](https://github.com/) account. Use your newschool username and email.
  - If you already have a GitHub account and repository under your newschool username, rename the repository to something else, then move on to step 2.
1. [Create a repository](https://help.github.com/articles/create-a-repo/) called `<YOUR_USERNAME>.github.io`, e.g. `fisherdm.github.io`

### Set up your local machine

#### Install Git

1. Open Terminal on your Mac `Applications > Utilities > Terminal`
1. Type `git` and press enter
1. Follow the instructions on screen to install OS X Dev Tools and Git
1. Once installed, type `git` again and you should see git's help text. This means it's installed correctly.

#### Create and add an SSH key to your GitHub account

1. [Create an SSH key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
1. [Add SSH key to GitHub](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

#### Set your Git username and email

1. `git config --global user.name "<YOUR NAME>"`
1. `git config --global user.email "<YOUR EMAIL ADDRESS>"`

#### Download and install software

1. [Sublime Text](https://www.sublimetext.com/)
  - If you have a preferred text editor you may use that instead.

### Set up your working repository

#### Clone your repository

```bash
cd ~                       # change directory to home directory
git clone <YOUR REPO PATH> # clone the new repo you created on GitHub
```

#### Upload your changes to the GitHub server

1. Create a file in your `<YOUR_USERNAME>.github.io` directory named `index.html`
2. Use git to add this file and commit the changes to GitHub:

```bash
git add .                    # tell git you want to add all files
git commit -m 'first commit' # commit these files with a message
git push                     # push these files to the remote server
```

### View your new website

Visit your new website at `http://<YOUR_USERNAME>.github.io`
