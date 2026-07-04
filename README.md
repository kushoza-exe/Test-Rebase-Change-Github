# Test-Rebase-Change-Github

1. Tried with rebase felt very complex , i dont know if it is a simple concept , but felt confusing as well, I might not use rebase bro.
2. Researched with another option, highlighting steps below.

*Option 1*: The Merge Approach (Recommended)This is the safest method. It brings the base branch changes into your new branch by creating a dedicated "merge commit".
1. Switch to your base branch (e.g., main or develop):bash *git checkout base-branch-name*
2. Pull the latest merged changes from the remote server:bash *git pull*
3. Switch back to your new branch:bash *git checkout your-new-branch*
4. Merge the base branch into your new branch:bash *git merge base-branch-name* *(git merge origin/main).*

Option 2: The Rebase Approach (Cleaner History)This method rewrites your new branch's history so that it looks like you created it after the new changes were merged into the base branch. Use this if you want a clean, linear commit history.
1. Fetch all recent updates from the remote repository: bash *git fetch origin.*
2. Make sure you are on your new branch: bash *git checkout your-new-branch.*
3. Rebase your branch onto the updated remote base branch: bash *git rebase origin/base-branch-name*

(Note: If you have already pushed your new branch to a remote server before doing this, you will need to use git push --force-with-lease to update it after rebasing)
