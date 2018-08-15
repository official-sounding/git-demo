# Tools Creating Repositories

## SourceTree
[SourceTree](https://www.sourcetreeapp.com/) is my git GUI of choice.  It is free, and it makes it very easy to do most operations you'd need to do on a git repository.  It also provides the ability to access less-common git activities in a reasonably user-friendly fashion.  I find it's history graph view particularly helpful to navigate between branches and to see the history of a repository.


## Git Command Line
Git also has a command line interface, that is unfortunately somewhat difficult to learn.  However, it remains the best way to perform some advanced tasks, and allows you to repair issues you may run across. I reccomend installing it, even if you plan to always use Sourcetree.  The [git-scm](https://git-scm.com/) website is a very good resource for using the Git command line utility, especially if you understand the nomenclature used in git.

# Terminology in Git

* a *repository* is a project that is set up in git.  It is contained in a specific folder.
* a *commit*, as a noun, is the core concept in Git.  It represents a single point-in-time of the repository, or a single set of changes applied to the repository.  The repository's history is made up a set of commits chained together in a graph.
* a *branch* is a label that points at a specific commit in the repository's history.
* to *checkout* is an action selecting a current branch to work on.
* the *working tree* is the branch that is currently checked out, and represents the current view of the repository in the file system (eg what you can see when you look at the folder in Explorer)
* a *remote* is another copy of the same repository stored somewhere else, either in another folder or on another computer that is linked to this repository.

# Committing Changes

## Staging
Staging Changes before commiting changes to git, you first need to "stage" them.  This ensures that a commit only captures the changes you want it to, and doesn't inadvertently include anything extra.  When staging via the command line, you can use the `git add` command.  SourceTree makes it very easy to select files for staging, and even allows you to stage "chunks", where only part of a file is committed

## Committing
After staging one or more files, you commit the changes to the repository.  This creates a commit nodes with your changes.  As a part of the commit, you attach a note indiciating what is contained in the commit.  git conventions are that the first 80 characters of the git message are a sort of "summary" of the change, and additional details can follow on later lines.

After committing, the commit will have a "commit id" associated with it, that will be a string of hexidecimal character.  the short version of this commit id is the first 6 characters in the commit id.  You can use this ID in various command if you need to refer to the commit.

## .gitignore

You can put a special file in your repository called `.gitignore` that allows you to exclude certain files from being added to the repository.  Wildcards can be specified in this file as well.  Any paths, filenames or wildcard paths specified in this file will be hidden from the SourceTree UI, and not be addable via the git command line.  This functionality can be useful for certain types of files that are sensistive, like environment-specific passwords, difficult to diff correctly (like images), or are otherwise ephemeral (the most common example being compiled source control).

# Branching

## It's all Just Commits
As mentioned above, a branch is literally just a label on a particular commit.  

## Moving Between Branches
When you want to work on a 

## Merging Branches

## Tags

# Remotes

## Push/Pull

## Don't Change History

# Fixing Stuff when it breaks

## Undoing commits at the end

## Undoing commits in the middle

## Amending commits

## git reflog
 