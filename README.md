# Git Tips
This is mainly just a list of git commands for my own reference

#### Key
- ```<COMMIT_HASH>```: the hash of a commit
- ```<N>```: a number
- ```<REMOTE>```: the name of a remote repository (most of the time the name is 'origin')
- ```<BRANCH>```: the name of a branch

---

### To undo the last commit...
#### and discard the changes from that commit:
```git reset --hard HEAD^```

#### and keep the changes from that commit:
```git reset --soft HEAD^```

### To undo the last N commits...
#### and discard the changes from those commits:
```git reset --hard HEAD~<N>```

#### and keep the changes from those commits:
```git reset --soft HEAD~<N>```

### To undo all commits made after the given commit...
#### and discard the changes from those commits:
```git reset --hard <COMMIT_HASH>```

#### and keep the changes from those commits:
```git reset --soft <COMMIT_HASH>```

### To squash the last N commits:
```git reset --soft HEAD~<N>```

```git commit -m "Your message"```

Force push to the origin
```git push origin +<BRANCH>```

### To sync a fork with the original repository:
Check if you have the upstream remote setup.
```git remote -v```

If not, then set up the upstream.
```git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git```

Fetch the changes from the upstream.
```git fetch upstream```

Make sure you're on your local master branch.
```git checkout master```

Merge the changes into your local repo's master branch.
```git merge upstream/master```

Push the changes to the origin remote.
```git push origin master```

### To fetch a remote branch (while also creating a local branch that tracks it)
```git checkout --track <REMOTE>/<BRANCH>```

### To delete a branch remotely
```git push --delete <REMOTE> <BRANCH>```

### To delete a branch locally
```git branch -d <BRANCH>```
