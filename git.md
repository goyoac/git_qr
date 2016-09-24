#GIT

git (locally) has a directory (.git) which you commit your files to
and this is your 'local repository'. This is different from systems
like svn where you add and commit to the remote repository
immediately.

### What means git push?

It means that files upload from the local repository to the remote repository.

### What means git fetch?

It means that files download from the remote repository to the local repository.

### What are the differences between 'git pull' and 'git fetch'?

In the simplest terms, git pull does a git fetch followed by a git merge

![Git Transport Commands](GITtransportcmd.png)

### Commands

- `git init` to initialize a Git repository
- `git status` to see what the current state of our project is
- `git add <filename>` to add a file to the staging area. The files in
  the Staging Area are not in our repository yet. We could add or
  remove files from the stage before we store them in the
  repository. Staging Area is place where we can group files together
  before we "commit" them to Git. Staged files are files we have told
  git that are ready to be committed.
- `git rm --cached <file>` to unstage
- `git reset` <filename> to remove a file or files from the staging area.
- `git commit -m "message describing what we've changed"` to commit
  files in staging area. A "commit" is a snapshot of our
  repository. This way if we ever need to look back at the changes
  we've made (or if someone else does), we will see a nice timeline of
  all changes.  
- `git log --summary` to see more information for each commit. You can
  see where new files were added for the first time or where files
  were deleted. It's a good overview of what's going on in the
  project.  
- `git remote add origin https://github.com/goyoac/git_qr.git` to push
 our local repo to the GitHub server. Previously we've created a new
 empty GitHub repository named `git_qr` with a `Readme.md` file. Git
 doesn't care what you name your remotes, but it's typical to name
 your main one `origin`.  
- `git pull origin master` to download `Readme.md`. This is no
  necessary in case we didn't include it during repository
  creation. Sometimes when you go to pull you may have changes you
  don't want to commit just yet. One option you have, other than
  commiting, is to stash the changes.  Use the command `git stash` to
  stash your changes, and `git stash apply` to re-apply your changes
  after your pull.
- `git push -u origin master` tells Git where to put our commits when
  we're ready. In this example we push our local changes to our origin
  repo (on GitHub). The name of our remote is `origin` and the default
  local branch name is `master`. The `-u` tells Git to remember the
  parameters, so that next time we can simply run `git push` and Git
  will know what to do.  
- `git diff HEAD` to look at what is different from our last
  commit. The HEAD is a pointer that holds your position within all
  your different commits. By default HEAD points to your most recent
  commit, so it can be used as a quick way to reference that commit
  without having to look up the SHA.  Using 'git diff' gives you a
  good overview of changes you have made and lets you add files or
  directories one at a time and commit them separately.  
- `git diff --staged` to look at what is different from staged files.  
- `git checkout -- <filename>` to change back to how they were at the
  last commit by using the command.  
- `git branch <branch_name>` to create a branch called
  `<branch_name>`. When developers are working on a feature or bug
  they'll often create a copy (aka. branch) of their code they can
  make separate commits to. Then when they're done they can merge this
  branch back into their main master branch.  
- `git checkout <branch_name>` to switch to branch <branch_name>. You
can use: `git checkout -b new_branch` to checkout and create a branch
at the same time.  
- `git rm <filename>` to delete files from the working tree. Use the
  `-a` option on `git commit` to remove deleted files with the
  commit. `git commit -am "Delete stuff"`  
- `git merge <brach_name>`  to merge the `<branch_name>` branch into `master` branch.  
- git branch -d <branch name> to delete a branch.  


  
- Pull Requests. If you're hosting your repo on GitHub, you can do
something called a pull request.  A pull request allows the boss of
the project to look through your changes and make comments before
deciding to merge in the change. It's a really great feature that is
used all the time for remote workers and open-source projects.  Check
out the
[pull request help page](https://help.github.com/articles/using-pull-requests)
for more information.



  
  

