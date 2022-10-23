## How to contribute 

* Fork the scikit-learn repo on GitHub ((https://github.com/scikit-learn/scikit-learn)[here])


https://scikit-learn.org/stable/developers/contributing.html

* This is the scikit-learn project repository: https://github.com/scikit-learn/scikit-learn.
  * To contribute, fork this repository. 
* My fork of scikit-learn: https://github.com/mdhornstein/scikit-learn-github-tutorial
* Clone the fork locally to disk: 
```
git clone https://github.com/mdhornstein/scikit-learn-github-tutorial
```
* Update conda: 
```
conda update conda 
``` 

https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes
* Viewing and adding remotes
  * Run `git remote` to see the shortnames of your remotes
    * "If you've cloned your repository, you should at least see `origin`-- that is the default name Git gives to the server you cloned from." 
  * Run `git remote -v` to see the shortname and url of each remote repository 
  * To add a new remote: `git remote add <shortname> <url>` 
* Pulling data from remotes 
  * `git fetch <remote>` fetches data but does not merge 
  * If your current branch tracks a remote branch, you can use `git pull` to download and merge data 
    * `git clone` sets up your local `main` branch to track the remote default branch 
* Pushing to remotes 
  * `git push <remote> <branch>` pushes your `<branch>` to the remote 

https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell
* A branch is a pointer to a commit. 
* Create a new branch: `git branch <branchname>` 
 * This does not switch to the new branch, it just creates the branch. 
* HEAD is a special pointer to a branch [i.e. a pointer to a pointer] 
* Display references (pointers) to each commit: `git log --decorate` 
* Switch to a different brandch: `git checkout <branchname>` 
 * This moves the HEAD pointer 
* "Switching branches changes files in your working directory" 


https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks
* "A fork is a copy of a repository" with two additional features: 
 * 
* The repository 

https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork
