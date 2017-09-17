# Understanding Git

The goal if this seminar is to promote a deeper understanding of the version
control software, git, so when you run in to issues down the road, you have a
strong basis for asking questions and searching for answers. 

## What is a commit?

A commit is specific set of additions/deletions (a patch). The current state of the code
can be reconstructed by applying the series of patches from the start of the
repository to any 
```
git add [NEW OR CHANGED FILE]
git commit [-m "commit description"]
```

## Branches and Merging

```bash
git branch
git checkout game-loop
git merge input-validation

# Edit main.cpp to fix merge conflicts
vim main.cpp

#recompile and validate program works

git add main.cpp
git commit
```

## Visualizing the Tree

Branches, tags, commit hashes are all just labels to nodes in a tree.

* Branches point to the ends of a series of nodes and are updated whenever you
  commit
* Tags point to a fixed commit (useful for labeling version numbers)
* Commit hashes reference the exact node. 
### Tools for Visualizing
* gitk (built-in)
* tig [Homepage](http://jonas.nitro.dk/tig/)
* GitHub -> Insight -> Graphs -> Network
* [More](https://git-scm.com/downloads/guis/)

## Rebasing vs. Merging

Rebasing is moving one branch onto the end of the other. Merging takes the ends
of the two branches and combines them. 

Rebasing allows for a simple linear history of the master branch. Merging is
simpler to implement but results in a messy history. 
* [Git Documentation](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
* [Example Network](https://github.com/previsualconsent/GitSeminarMergeRebase/network)


## Remotes (Push and Pull)

With Git, each repository can contain the full history. There doesn't have to be
a central repository

```
git remote add local /path/to/local/repo
git remote add ssh-server ssh://user@server/project.git
```

### Pull

Use `git pull` to update the local branch from the remote repository. A pull is a
fetch (update local references to remote repositories) and then a merge. 

### Push

Use `git push` to send your local changes to a remote. This can either create a
new branch or "fast forward" the remote branch to where your local branch is. 

### GitHub
We commonly use GitHub to host the repositories and it acts as a central server.

Forking a repository on the website is cloning into your GitHub account. 

On GitHub, use Pull Requests to offer your own contributions to other projects. 

My favorite GitHub work flow is push to always push updates to a new remote
branch, then use the GitHub Pull Request to merge them into master. 
