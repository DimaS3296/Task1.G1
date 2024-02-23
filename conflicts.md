[< to Table of Contents](./readme.md)

Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict. Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.

#### To avoid conflict

The more you change in a file, the greater the potential for conflict.  Make more commits with fewer changes each.  Avoid making a large change that combines multiple feature enhancements or bug fixes into one. 

#### To resolve a conflict: 
Step 1: The easiest way to resolve a conflicted file is to open it and make any necessary changes.

 Step 2: After editing the file, we can use the git add a command to stage the new merged content.
 
Step 3: The final step is to create a new commit with the help of the git commit command.

 

There are many tools to help resolve merge conflicts. Git has plenty of command line tools such as :  [git log](./log.md),  [git status](./status.md),  [git checkout](./checkout.md), and [git reset](./reset.md). 

And  learn to use [git rebase](rebase.md).

In addition to the Git, many third-party tools offer streamlined merge conflict support features.

