# So, what is Git?
Snapshots

Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

## Local Operations

Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

## Tracking Changes

Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

## Loss of Data

Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

## States

Files in Git can reside in three main states: committed, modified and staged.

Committed

Dat---a is securely stored in a local database

Modified

File has been changed but not committed to the database

Staged

Flagged a file’s changed version to be committed in the next snapshot

## What to do with git

Cloning
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:
`$ git clone https://github.com/test`
By cloning the file, you have copied all versions of all files for a project.

## Local Repository Structure

The local Git repository has three components:

Working Directory: The actual files reside here.
Index: The area used for staging
Head: Points to the most recent commit

## Check File Status

To determine the state of files, utilize the git status command:
`git status`
this will tell you if there are updates that need to be pushed to the directory

## Tracking and Staging a New File

Single File

Track one file only by using the following format
`git add filename`
For all files 
`git add .`
to commit files 
`git commit -m:"whatever change you made"`
to push to directory
`git push origin main`

## Remote Repositories

In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

### Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

### Seeing Your Remotes
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.
`cd example`
`git remote -v`
remote1 https://github.com/remote1/example (fetch)

remote1 https://github.com/remote1/example (push)

remote2 https://github.com/remote2/example (fetch)

remote2 https://github.com/remote2/example (push)

remote3 https://github.com/remote3/example (fetch)

remote3 https://github.com/remote3/example (push)


[Back to Home](../README.md)