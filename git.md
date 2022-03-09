### Basic git commands

Find all the basic commands in this [Github repo](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches)

### Checkout to a remote branch
- Checkout to a remote branch by tracking it : `git checkout --track <REMOTE_BRANCH>`

### Merge current branch with master
- If you want to up-to-date your local branch with the master branch, use the following commands: 
  `git checkout <LOCAL_BRANCH>`
  `git merge origin/master`

### Remove local and remote branch

#### Local branch
-First, we print out all the branches (local as well as remote), using the git branch command with -a (all) flag.
-To delete the local branch, just run the git branch command again, this time with the -d (delete) flag, followed by the name of the branch you want to delete (test branch in this case).

>Note: You can also use the -D flag which is synonymous with --delete --force instead of -d. This will delete the branch regardless of its merge status.

#### Remote branch

To delete a remote branch, you can’t use the git branch command. Instead, use the git push command with --delete flag, followed by the name of the branch you want to delete. You also need to specify the remote name (origin in this case) after git branch.

>git branch -a

*master

test

remote/origin/master

remote/origin/test

>git push origin --delete test

### Ignore files in Git

Follow the link : https://help.github.com/en/github/using-git/ignoring-files

To remove all the .DS_Store files follow this stackoverflow answer: https://stackoverflow.com/questions/18393498/gitignore-all-the-ds-store-files-in-every-folder-and-subfolder


If you wish to have a public repo of your codebase along with a private repo, here is the best strategy: https://stackoverflow.com/questions/7983204/having-a-private-branch-of-a-public-repo-on-github


### Stashed by mistake? Don't worry!
- If you have stashed you uncommitted changes by mistake, and want to get back those in the same state, use the following commands: 
  `git stash apply <stash_ref>`

### Stacked Feature Development
- You can start a branch from another branch using the following commands:
  `git checkout -b <new_branch_name>`
- Remember to rebase with the parent branch before commit in the child branch.
- During review, pass the parent branch name using the following command:
  `git review create --parent=<parent_branch_name>`
  `git review update --parent=<parent_branch_name>`
- Post merge with master branch, you need to remove the commit history using the follwing command:
  `git rebase -i master`
- If you make any mistake while rebase, us the following command to get rid of the issue:
  `git rebase --abort`
