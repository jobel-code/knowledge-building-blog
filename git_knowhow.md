# Using git

See good practices advice in:
- [Google developer-workflow](https://github.com/googledatalab/datalab/wiki/Developer-Workflow)



```
git config --global user.name "Your Name"
git config --global user.email your@email.address
```

# Typical feature development

```
# Get to a clean initial state and then create your feature branch
cd <your local repository>
git checkout master
git pull --rebase --prune
git checkout -b <branch name>

# Work on your changes and commit locally
git add .
git commit -m "Short descriptive text"
...

# Keep pushing your changes to origin, so they're generally visible
git push -u origin <branch name>

# Stay in sync with master, and push to your branch/fork
# often as you progress.
# First get all of your changes down to a single commit (if
# it makes sense to treat all individual commits as atomic)
git rebase -i origin/master
git checkout master
git pull --rebase
git checkout <branch name>
git rebase master
git pull --rebase
git push -u origin <branch name>
...

# Once ready for review, submit a pull request via GitHub.
# Make sure you've followed style guidelines, added and run
# tests as appropriate.
# Address feedback and review comments by committing
# locally and pushing (to update the pull request)

# Cleanup your local history to prepare for merging
git rebase -i origin/master
git push --force origin <branch_name>
```

# Branches

Here is the simple naming convention when creating branches:

* `feature/<feature_name>` - for feature sized work
* `issues/issue_#` - for addressing specific issues
