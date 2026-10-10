# GTDSAA - Georgia Tech Data Structures and Algorithms

The Data Structures and Algorithms Professional Certificate from GTx is a four-course series covering the foundations of data structures, and designing efficient algorithms. 

**Course**: [https://www.edx.org/certificates/professional-certificate/gtx-data-structures-and-algorithms](https://www.edx.org/certificates/professional-certificate/gtx-data-structures-and-algorithms)

## Course Progress: 5.2%

- [x] 01 - Data Structures & Algorithms I: ArrayLists, LinkedLists, Stacks and Queues

## Course content

## Repository configuration

Each submodule in this repository contains the code examples of the original course.

### Create new submodules

Create a new repository on Github, then execute the following commands to link the new repository as a submodule of the main repository:

```
$ cd georgia-tech-data-structures-and-algorithms
$ git submodule add -b main git@github.com:ensomugnog/gtdsaa-submodule
```

Using the **-b** argument means we want to follow the main branch of the new repository, and after running this command we’ll have a new directory named `gtdsaa-submodule/`, this directory will automaticaly checkout the main branch for you to be ready to make changes.

### Update main repository with latest submodule changes

First make sure the submodule changes have been commited and pushed to the orign repository, then run the following commands:

```
$ git status
$ git stage .
$ git commit -m 'gtdsaa-submodule'
$ git push
```

### Clone Repository with submodules

If you want to clone a repository including its submodules you can use the --recursive parameter, use the --jobs parameter to fetch multiple submodules at the same time, download up to 8 submodules at once use --jobs 8

```
$ git clone --recursive --jobs 8 git@github.com:ensomugnog/georgia-tech-data-structures-and-algorithms.git
```

### Delete a submodule from a repository

Currently Git provides no standard interface to delete a submodule. To remove a submodule `gtdsaa-submodule` you need to:

```
$ git submodule deinit -f gtdsaa-submodule
$ rm -rf .git/modules/gtdsaa-submodule
$ git rm -f gtdsaa-submodule
```

### Checkout a commit

To checkout a Git commit, you will need the commit hash.

```
$ git checkout 4aa03973d004286558465a8d86bcccfdc7b46505
$ git reset --hard
$ git checkout main
```