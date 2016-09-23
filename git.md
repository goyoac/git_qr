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
  before we "commit" them to Git.
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
