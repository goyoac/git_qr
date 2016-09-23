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
