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

## Rebasing vs. Merging

* [Git Documentation](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)
* [Example Network](https://github.com/previsualconsent/GitSeminarMergeRebase/network)


## Remotes (Push and Pull)

