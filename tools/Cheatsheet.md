
# Git commands

This sheet aggregates useful commands when using git from the command line. 

## Routine commands
```
git status
git add <file>
git commit -m <informative message>
```
## Additional useful commands

### Creating and checking out of a branch simultaneously

```
git checkout -b <new_branch>
```

### Git fetch versus git pull

* `git fetch` downloads the changes from the remote but does not merge them into your working branch. It just updates your remote-tracking refs (e.g. origin/main). You stay on your current code untouched.

* `git pull` does a fetch and immediately merges (or rebases) the changes into your current branch. It's essentially git fetch + git merge in one step.

```
# fetch: safe, just downloads
git fetch origin
git diff main origin/main   # inspect what changed before merging
git merge origin/main       # merge when you're ready

# pull: fetch + merge in one go
git pull origin main
```

## amend commit
```
git commit --amend -m "message"
pit push --force # if commit already pushed
```

### revert commit with message
```
git revert --no-commit <commit hash>
git commit -m "commit message"
```