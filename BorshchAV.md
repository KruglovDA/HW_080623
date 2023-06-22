# Git quick guide

## __Introduction__

A version control is a kind of system which allows you to keep track of the changes that have been made to a code over a duration of time. Using version control system software (VCSs) man can revert back to the older versions, rectify mistakes, work with a team on a shared folder, etc.
Git happens to be a one of thr most popular VCSs. Git is a distributed (peer-to-peer) VCS, unlike centralized ones, so the changes are made in a localized repository, it's more fast, simple and efficient. 

## __Installing__

Check whether your operating system already contains Git: open your terminal application and type "git version". The output should tell you which version Git is installed.If you get "a foreign command", you will have to install Git manually.

 If you have already installed Git, you should be able to acquire the latest development versions from Git via code: 

 *git clone https://github.com/git/git*.

 ## Creating a repositiory

 1. *git init* - creating a new *(previously non-existing)* local repository. This creates a new subdirectory named **.git** that contains all your nesessary repository files.
 2. *git clone URL* - creating a copy (cloning) of a remote repository. For example: git clone https://github.com/abcgit/abcgit.

 ## Repository changes 

 1. *git status* - determines which files are in which state in .git, which branch you're on.
 2. *git add .* - tracks a new file, stages the latest version of the file.
 3. *git commit -m "commentary"* - creates commit and type a message about changes in quotes.

5. *git diff* - shows the differences between the current version of the file and the previous one.

6. *git log* - lists the commits in the repository in reverse chronological order with their comments and checksums of commits.
    * _q_ - quit from the list making by *git log*.

    * _git log **first four characters of commit's checksum**__ - moving to the commit indicated by these characters.
    * _git log --graph_ - show commit logs with graphical view.

## Ignoring /removing files

1. *.gitignore* - specifies intentionally untracked files that Git should ignore.

2. *git rm __path__* - remove files from the working tree and from the index; the command removes only the paths that are known to Git.

## Branching

   1. *git branch* - shows the list of all existing branches and indicate what branch you are on.

   2. *git branch __branch_name__* - creates the new branch.

      * _git branch -d **branch_name**__ - delete branch _**branch_name**_.
  
   3. *git checkout __branch_name__* - moving from the current branch to the branch *__branch_name__*.

   4. *git merge __branch_name__* - merging branches; branch *__branch_name__* join (flows in) current branch.

   # Working with remote repositories

   ## Creating a remote repository from the command line

   *git remote add [name] [URL]* - add a remote named [name] for the repository at [URL].   
   
   ## Another ways to create a local repository or modifying it
   
   *git clone [some-url]* - download the entire existing repository, initialize a local repository on disk, checkout the default branch into the workspase and create a pointer to the remote repository named *origin*.

   *fork* - a GitHub command, which copies any publicly available repository to your GitHub account. Then you can clone this repository on disk.

   *git pull* - not only fetch from but also integrate with another repository or a local branch.

   ## Synchronizing

   *git push* - upload local repository content to a remote repository.
   
   * _git push [origin] [branch_name]_ - push the specified branch, along with all of the necessary commits and internal objects, to the branch [origin] of the remote repository.
   * _git push --set - upstream [origin] [branch_name]_ - creates automatically branch [branch_name] in the remote repository if it doesn't already exists.



