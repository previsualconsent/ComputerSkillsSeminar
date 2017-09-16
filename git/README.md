# Understanding Git

The goal if this seminar is to promote a deeper understanding of the version
control software, git, so when you run in to issues down the road, you have a
strong basis for asking questions and searching for answers. 

## What is a commit?

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

## Rebasing vs. Merging

## Remotes (Push and Pull)

