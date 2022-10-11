# git Documentation 
In this document, we go through the best practices when using git.
## setting up the SSH keys:
Use [GitHub SSH key setting](https://github.com/settings/keys) to set up your SSH key to use. After you have done setting it up, you should be able to clone, push, etc. Make sure to use the SSH link when you are interacting with GitHub repositories.

## Branching Strategy:
Each user should work on their branch (other than main/master) and avoid conflicts, it is recommended that each person works on different files to avoid conflicts.
## Merge Strategy:
No merging to master should be directly allowed. Each merging to master should be done through a pull request, in which the changes are reviewed by the lead.
If the master is ahead of the branch, use git rebase first, and then merge into master.
### Merging to master branch procedure:
If you are using Visual Studio Code you can change git editor by 
```console
git config --global core.editor "code --wait"
```
In case you are using Pycharm consider using [Pycharm rebase documentation](https://www.jetbrains.com/help/pycharm/apply-changes-from-one-branch-to-another.html#rebase-branch)
You can change code with the editor of your choice. The proposed merging procedure is given below:
```console
- git switch to_be_merged_branch
- git pull
- git rebase master -i
- git push --force
```
In the [rebase](https://git-scm.com/docs/git-rebase) step, try to clean the commit history of your code. In the next step open GitHub and open a pull request and add the respective reviewers.
## Commit Strategy: 
Commit messages should follow one of the followings:
- **feat**: A new feature
- **fix**: A bug fix
- **style**: Additions or modifications related to styling only
- **refactor**: Code refactoring
- **test**: Additions or modifications to test cases
- **docs**: README, Architectural, or anything related to - documentation
- **chore**: Regular code maintenance
