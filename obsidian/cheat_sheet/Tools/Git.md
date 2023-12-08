[ ] Test git-flow
[ ] 
[ ] 
---
---


# GitHub Actions

Automate, customize, and execute your software development workflows right in your repository with GitHub Actions. You can discover, create, and share actions to perform any job you'd like, including CI/CD, and combine actions in a completely customized workflow.

## Basic commands

| Git Command | Comment |
| --- | --- |
| `git init` | Initialize a directory as git managed repository |
| `git clone <url>` | Clone a remote repository to your local client |
| `git status` | Shows uncommited changes, new files etc. |
| `git add <file>` | Stage an updated / new file to the next commit |
| `git rm <file>` | Remove a file and stage the removal for the next commit |
| `git commit -m "message"` | Commit staged changes under a new commit |
| `git commit` | Will open an editor to write more descriptive commit messages. See [here](https://cbea.ms/git-commit/) for a guide on good commit messages |
| `git log` | Shows a list of commits in the current branch |
| `git log --pretty=oneline` | Shows a list of commits in the current branch in one line |
| `git log --patch` | Shows a list of commits in the current branch with the changes |
| `git reset <commit>` | Reset the current branch to the given commit |
| `git reset --hard <commit>` | Reset the current branch to the given commit and discard all changes |
| `git reset --soft <commit>` | Reset the current branch to the given commit and keep all changes staged |
| `git checkout <branch>` | Switch to another branch |
| `git branch` | Shows a list of existing branches |
| `git branch <branch>` | Creates a new branch (from the currently checked out branch) |
| `git merge <branch>` | Merge changes from `branch` to the currently checked out branch |
| `git push` | Push commited changes to the remote repository |
| `git pull` | Pull current state from the remote repository to your local repo |
## New installation
## Linux

On Linux, Git can be easily installed on Linux systems with the available package managers.

E.g. for Debian based systems:

```sh
apt install git
```
## Windows

On Windows, Git can be installed by downloading the installer from the [download page of Git](https://git-scm.com/downloads).

Or by using the winget package manager:

```pwsh
winget install git
```


### Basic commands

| Git Command | Comment |
| --- | --- |
| `git init` | Initialize a directory as git managed repository |
| `git clone <url>` | Clone a remote repository to your local client |
| `git status` | Shows uncommited changes, new files etc. |
| `git add <file>` | Stage an updated / new file to the next commit |
| `git rm <file>` | Remove a file and stage the removal for the next commit |
| `git commit -m "message"` | Commit staged changes under a new commit |
| `git commit` | Will open an editor to write more descriptive commit messages. See [here](https://cbea.ms/git-commit/) for a guide on good commit messages |
| `git log` | Shows a list of commits in the current branch |
| `git log --pretty=oneline` | Shows a list of commits in the current branch in one line |
| `git log --patch` | Shows a list of commits in the current branch with the changes |
| `git reset <commit>` | Reset the current branch to the given commit |
| `git reset --hard <commit>` | Reset the current branch to the given commit and discard all changes |
| `git reset --soft <commit>` | Reset the current branch to the given commit and keep all changes staged |
| `git checkout <branch>` | Switch to another branch |
| `git branch` | Shows a list of existing branches |
| `git branch <branch>` | Creates a new branch (from the currently checked out branch) |
| `git merge <branch>` | Merge changes from `branch` to the currently checked out branch |
| `git push` | Push commited changes to the remote repository |
| `git pull` | Pull current state from the remote repository to your local repo |
## Initial steps

- Create project folder from /home

```shell
mkdir /home/project/izi
```
Git can be configured by the CLI using the `git config` command. For first configuration it is necessary to configure at least the parameters `user.name` and `user.email`. This
can be done by the following commands:

```bash
git config --global user.name "MyFancyUser"
```

```bash
git config --global user.email "developer@mydomain.com"
```

### Initialize a directory as git managed repository and pull from remote repo
```bash
git init
```
Set a new repo.
```bash
git remote add upstream "remote repository address"
```
Confirm new remote repo.
```bash
git remote -v
```  
Get branches. 
```shell
git fetch upstream 
```
Shows a list of existing branches  
```shell
git branch -va
```  
Pull current state from the remote repository to your local repo
```shell
git pull "remote repo address"
```
check log 
```shell
git log
```

### Local push to remote (Master)

Create a random file (inside local .git folder)
```shell
echo "stunning-octo-happiness" >> README.md
  git add README.md
  git commit -m "first commit"
  git log
  git status
  git push -u origin main

```


---

### Working with git-flow

^1c6c35

Git-flow assists you by combining multiple steps of `git` commands to one `git-flow` command
which will do a workflow of steps. Although `git-flow` makes live easier in some cases,
it makes it also more complex sometimes and you need to execute some steps before or after using
a `git-flow` command as regular `git` command. (See below)

As an example, here is the comparison between the regular `git` commands and the appropriate
`git-flow` command for creating a release.

| git-flow command                                    | git command                                           |
| --------------------------------------------------- | ----------------------------------------------------- |
| `git-flow feature start <feature_name>`             | `git checkout -b feature/<feature_name> develop`      |
| `git-flow feature finish <feature_name> [--squash]` | `git checkout develop`                                |
|                                                     | `git merge [--squash] --no-ff feature/<feature_name>` |
|                                                     | `git branch -d feature/<feature_name>`                |

Another `git-flow` cheat sheet can be found [here](https://danielkummer.github.io/git-flow-cheatsheet/).
## Events


---
## Jobs


---
## Actions


---
## Runners

A runner is a server that runs your workflows when they're triggered. Each runner can run a single job at a time. GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run your workflows; each workflow run executes in a fresh, newly-provisioned virtual machine.
