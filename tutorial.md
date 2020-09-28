# Git Tutorial

## Installation and getting started

In this lab, you will:

* Install the Git command line interface
* Verify your Git version
* Explore Git help
* Configure your user name, email address and default Git editor

### Install the Git command line interface

If you have not installed Git, please use [these instructions](https://www.atlassian.com/git/tutorials/install-git).

### Verify your Git version

Open a command line and verify that Git is installed.

```git
git --version
```

### Explore Git help

View overall Git help by typing

```git
git
```

at the command line.

Choose any Git command that you see and view the help on it using

```git
git help <command>
```

For instance,

```git
git help init
```

View concise help on a command using the `-h` option. For example,

```git
git init -h
```

### Configure your user name, email address and default Git editor

View your current setting for your user name with

```git
git config user.name
```

If you would like to change your user name, use

```git
git config --global user.name "FIRST_NAME LAST_NAME"
```

View your current setting for your email address with

```git
git config --global user.email "YOUR_NAME@example.com"
```

View your current setting for default Git editor with

```git
git config core.editor
```

If you would like to change your default Git editor, use

```git
git config --global core.editor your_preferred_editor
```

Note that **nano** seems to be a good editor for people who have not used **vi** or **vim**. Other options are **Notepad++** (Windows) or **Atom**. Make sure that you install your editor before configuring it her.

## Commit to a local repository

In this lab, you will:

* View file status using `git status`.
* Stage content using `git add`.
* Commit content using `git commit`.
* View the commit history using `git log`.

### View file status using `git status`

Create `repos`, by running:

```bash
mkdir repos
```

Change to the `repos` directory, by using:

```bash
cd repos
```

Create `projecta`, by running:

```bash
mkdir projecta
```

Change to the `projecta` directory, by using:

```bash
cd projecta
```

Execute

```git
git init
```

to initialize Git in the current directory.

Execute

```git
git status
```

to view the file status. You should see the message "Nothing to commit".

Create an empty file named `fileA.txt` in the `projecta` directory, by using:

```bash
touch fileA.txt
```

This is the first file in your working tree.

Execute

```git
git status
```

to view the file status. You should see that Git notices the `fileA.txt` file and identifies it
as untracked.

### Stage content using `git add`

Add `fileA.txt` to the staging area, by using:

```git
git add fileA.txt
```

Again, execute

```git
git status
```

You should see that Git adds `fileA.txt` under "Changes to be committed".

### Commit content using `git commit`

Execute

```git
git commit -m "add fileA.txt"
```

to create a commit. The `-m` option adds a commit message.

### View the commit history using `git log`

Execute

```git
git log
```

You should see your commit details, including your commit message.

Execute

```git
git log --oneline
```

A concise version of the history is displayed.

## Create a Remote Repository

xxx

## Push to a Remote Repository

In this lab, you will:

* Clone your Bitbucket repository.
* Create a commit in the local repository.
* Push the commit to the remote repository.

Paste the `git clone` command that you copied, and execute this command

```git
git clone https://demirelbu@bitbucket.org/demirelbu/projectb.git
```

to clone the **empty** repository.

Change to the `projectb` directory by using

```bash
cd projectb
```

View the contents of `projectb` folder by using

```bash
ls -al
```

Execute

```git
git remote -v
```

You should see the URL to your remote repository, and see that the shortcut name of this remote repository is `origin`.

Execute

```bash
echo "# projectb's README" > README.md
```

in your projectb directory.This creates a README file in your working tree.

Execute

```git
git add README.md
```

to add the README file to the staging area.

Execute

```git
git commit -m "add README.md"
```

to commit to the local repository.

Execute

```git
git push -u origin master --dry-run
```

The `-u` flag sets up the local and remote branches as tracking branches. The `--dry-run` flag makes a rehearsal for executing `git push`. `origin` is a shortcut name for the remote repository. `master` is the branch to push.

Execute

```git
git push -u origin master
```

to track remote branch `master` from `origin`.

Execute

```git
git status
```

and verify that your branch is up-to-date and there is **nothing to commit.**

## XXXXX

In this lab, you will:

* Create, push and view references of a commit.
* Tag the commit.

Change to the `projectb` directory by using

```bash
cd projectb
```

Execute

```bash
echo "feature 1" > fileA.txt
```

to create a file named `fileA.txt` containing the simple string "feature 1".

Execute

```bash
ls -al
```

to **list** the contents of `projectb` folder.

Execute

```git
git add fileA.txt
```

to **add** `fileA.txt` to the staging area.

Execute

```git
git commit -m "add feature 1"
```

to **commit** this file to the local repository by specifying a commit message of "add feature 1".

Execute

```git
git push origin master
```

to **push** the commit to the remote repository.

Execute

```git
git log --oneline
```

to **view** your local repository's commit history. Notice that the SHA-1 values of the commit objects have been shortened. Also notice that there are labels/references associated with the commit(s). Labels starting with `origin` are related to the remote repository.

Execute

```git
git show
git show HEAD
git show master
```

Execute

```git
git tag
```

to **view** the tags in your local repository. **There should be no tags.**

xxxxxxx [2.]

Execute

```git
git tag
```

again to **view** the tags. **You should see your "v0.1" tag.**

Execute

```git
git show v0.1
```

Execute

```git
git push origin v0.1
```

to **push** the tag to the remote repository.

### Tag the commit

Execute

```git
git tag
```

to **view** the tags in your local repository.



## Resolving Merge Conflicts
