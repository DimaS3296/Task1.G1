[< to Table of Contents](./readme.md)

## git rebase 

**git rebase *[file]*** - Rebase is one of two Git utilities that specializes in integrating changes from one branch onto another.

 The other change integration utility is [git merge](./merge.md).
 Merge is always a forward moving change record. Alternatively, rebase has powerful history rewriting features.

 [git merge](./merge.md)
 can develop a new commit that can integrate the changes from two branches. This new commit has two parent commits, one from each branch. Git rebase, execute the changes from one branch onto another and explore it as though the changes were made directly on that branch.

 The primary reason for rebasing is to maintain a linear project history.

 Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most useful and easily visualized in the context of a feature branching workflow. 

 Use command:
```bash=
git rebase.
```