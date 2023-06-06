# Git In-depth

## Git Foundations
### Data Storage
Git stores the data in a key-value way using SHA-1 encryption.
Git data is stored in the .git directory
A commit points to a tree and contains the following metadata:
* Author and committer
* Date
* Message
* Parent commit (one or more)

The SHA-1 of the commit is the hash of all this information above

### blob
the contents encrypted using SHA-1

![image](https://github.com/Unosquare-CoE-JavaScript/fabian-rojas/assets/132394353/b7f1dd50-c665-4e08-a61d-84c2278884c8)

### tree
Data structure that contains pointers to blobs or to other trees.

![image](https://github.com/Unosquare-CoE-JavaScript/fabian-rojas/assets/132394353/f2fdb08c-efc6-4b22-ba93-afa0a349c34f)


## Git Areas
### Working Area
Also called untracked files, the changes made since last commit, but not ready to be sent to the repository yet.
### Staging Area
Changes ready to be sent to the repository.
### Repository
Files, branches and commits ready to be pulled and worked on.


## Git References
### References
A branch is a pointer to a particular commit.
### Head
It is how Git knows what branch you're currently on.
### Tags
* Lightweight tags are just a simple pointer to a commit.
* Annotated tags point to a commit but with some additional information.

### Dettached head
When a chekout is made to a commit different that the HEAD, is called a dettached head and will be collected by the garbage collector.


## Merging and Rebasing
### Git merge
* Fast forward: adding changes to tip of target branch
Git RERERE ➡️ Reuse Recorded Resolution
### Git rebase
Changes the parent of a commit.

## Git History and Diffs
* Good commits help to preserve the history of a codebase
* A single line commit is not always the most descriptive

### Git log
Show the history of the branch.

### Git diff
Shows the files that have been changed since the last commit.

### Git remotes
Is where the local repository gets the data from, also can point to the same remote or a different one.

## Useful commands

### Git checkout
Restore working tree files or switch branches.

#### Internal steps when doing a checkout
1. Change HEAD to point to a new branch.
2. Copy commit snapshot to staging area.
3. Update the working area with the branch contents.

🚧 Git checkout is sometimes an unreversable operation 🚧

### Git clean
Will remove untracked files

### Git reset
For commits ➡️ Moves the HEAD pointer, optionally modifies files.

For file paths ➡️ Does not move the HEAD pointer, modifies files.

### Git revert - *The "safe" reset*
Creates a commit undoing changes from a previous commit.

### Git stash
Stores changes since the last commit into an isolated location like saving changes for later.

### Git amend
Allows to add changes to a previous commit.
