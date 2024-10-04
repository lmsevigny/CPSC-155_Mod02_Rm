# Ch2.2
# Exercise: No Longer Track with Git (but still Keep on Disk) a File that Was Accidentally Committed

## Step 1
Familiarize yourself with the repository by checking the file structure, file contents, etc.

## Step 2
You can confirm that file `file_alpha_that_should_not_be_tracked_by_git.class` is being tracked by Git using the following commands:
```bash
$ echo "some change" >> file_alpha_that_should_not_be_tracked_by_git.class
$ git status
```
The git status should indicate that the file was modified, confirming that it is under git's control.

To discard the change made to the file (and to restore the repository to the same status as when it was cloned), run the following commands:
```bash
$ git checkout -- file_alpha_that_should_not_be_tracked_by_git.class
$ git status
```

## Step 3
File `file_alpha_that_should_not_be_tracked_by_git.class` was accidentaly staged and committed to the git repository in a previous commit and we would like to rectify this action, by keeping the file on disk, but removing it from git's control (i.e., file can be modified locally, but git will no longer care what changes are being made to it).

What **git command** do you need to issue to remove the file `file_alpha_that_should_not_be_tracked_by_git.class` from git, but still keeping it on disk?

HINT: After running this **git command** and issuing a `git status`, the file `file_alpha_that_should_not_be_tracked_by_git.class` should appear in two places:
* in the staged area (as deleted)
* in the untracked files
