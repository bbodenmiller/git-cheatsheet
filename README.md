# Git Cheatsheet #

## Merge ##
### Merge all changes from another branch using rebase ###
If branch is on remote you'll need to run
> `git fetch <remote>`
And modify `<branch>` below to be `<remote>/<branch>`

Pulls changes from other branch in to our branch and then applies our changes on top of that.
> `git rebase <branch>`

### Merge all changes from another branch ###
> `git merge <branch>`

### Merge one commit from another branch ###
> `git cherry-pick <commit>`

### [Two repositories](http://blog.caplin.com/2013/09/18/merging-two-git-repositories/) ###

## Undo ##
### Undo uncommitted changes ###
Remove staged and working directory changes

> `git reset --hard`

Remove untracked files

> `git clean -fd`

### Undo commit but leave changes ###
> `git reset --soft HEAD~1`

Where `1` can be replaced with the number of commits you want to undo.

### Undo commit & remove changes ###
> `git reset --hard HEAD~1`

Where `1` can be replaced with the number of commits you want to undo.

## Push code ##
### Push tags to remote server ###
> `git push --tags`

### Force push ###
Overwrites all changes on server with your changes. This should never be used if others are writing to branch also.
> `git push -u -f`

### Show all remotes ###
> `git remote -v`

## Resources ##
* [Another Git cheatsheet](https://github.com/jasonniebauer/git-cheatsheet)
