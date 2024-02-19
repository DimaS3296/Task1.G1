[< to Table of Contents](./readme.md)

## git stash

**git stash *[file]*** - To save changes made when they’re not in a state to commit them to a repository. This will store the work and give a clean working directory. For instance, when working on a new feature that’s not complete, but an urgent bug needs attention.

The git stash command will help a developer switch branches to work on something else without committing to incomplete work.

use command:
```bash=
git stash
```

Usage

### Store current work with untracked files
$ git stash -u

### Bring stashed work back to the working directory
$ git stash pop
