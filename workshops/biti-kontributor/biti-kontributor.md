# 15:00-15:30: Workshop - Kako biti kontributor?
- Speaker: Adnan Rahić - Dev, teacher & mentor @ Bookvar
- Kako biti contributor?
- Kako napraviti pull request?

https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github

### Intro
Git 
- Version control software 
- makes projects manageable

Open source projects 
- hosted in public repositories
- benefit from contributions made by the developer community
- pull request => request that a project accepts changes you have made to it

This workshop will:
- show you how to make a pull request
- show you how to contribute to open source projects

### Prerequisites
Have Git installed
Have a GitHub account
Find a GitHub repository to contribute to

### Forking - Create a copy of the repo
A repo is the main folder of the project
Forking - copy the repo to your GitHub Account
**demo**
Go to - https://github.com/TheAdnan/focustube
Click fork!
Will get forked to - https://github.com/your-username/focustube

### Cloning
Making a local copy of the repo
Similar to URL above, only ends with .git - https://github.com/TheAdnan/focustube.git
**demo**
```bash
$ git clone https://github.com/TheAdnan/focustube.git
```

### Branching
Used to manage workflow
Used to control new features and which will make it back to the main branch
Default main branch - `master`
Best practice - anything on `master` is deployable
Creating a branch 
 - from `master`
 - give a descriptive name

**demo**
```sh
$ cd repository
```
```sh
$ git checkout -b new-branch
```
```sh
$ git checkout master or some-other-branch
```

### Making local changes
After making local changes they need to be added and committed

**demo**
```sh
$ git add -A  
```
```sh
$ git commit -m "Fixed documentation typos"
```
```sh
$ git status
```
```sh
$ git push --set-upstream origin new-branch
```

### Update local repo
Add a remote - a remote is a version of the repo on the internet
The remote will reference the original repo - sync changes between your fork and the original repo

**demo**
```sh
$ git remote -v
```
```sh
$ git remote add upstream https://github.com/original-owner-username/original-repository.git
```

`upstream` is the shortname we have supplied for the remote repository - in Git it references the repo we cloned from

Sync the fork - get the latest files from upstream

```sh
$ git fetch upstream
```

Checkout your local master branch
```sh
$ git checkout master
```

Merge the changes from the original repo
```sh
$ git merge upstream/master
```

Now your fork's master is synced with the original repo's master. Go ahead and sync your forks master with your branch.
```sh
$ git checkout new-branch
$ git merge master
```
Now you've avoided conflicting code because you're making sure your local branch is up to date with the upstream's master.

### Create a Pull Request
Navigate to forked repo - press "New pull request".
Choose what branch include in the pull request.

**demo**
show:
- go to forked repo and press pull request
- go to original repo and show pull request option