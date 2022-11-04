--- 
layout: post 
author: michael 
--- 

# Contributing to scikit-learn 

## Table of contents 
* [How to contribute](#how-to-contribute)
   * [Initial setup](#initial-setup) 
   * [Working on an issue](#working-on-an-issue)
   * [Getting your changes "accepted"/merged](#getting-your-changes-accepted)

## How to contribute 

In this section, we extract the relevant steps from the scikit-learn Contributing tutorial, and put them all in one place, sequentially. Most 

### Initial setup 
* Fork the scikit-learn repo on GitHub ([here](https://github.com/scikit-learn/scikit-learn)). 
    * This creates a copy of the repo in **your** GitHub account. 
* Clone the repo to your local disk, using the URL visible in the Code dropdown menu in the upper right. 
* (For mac OS) Create a virtual environment with the build dependencies and with a compiler with OpenMP support. 
    ```
    conda create -n sklearn-dev -c conda-forge python numpy scipy cython \
        joblib threadpoolctl pytest compilers llvm-openmp
    conda activate sklearn-dev
    ```
* Build the project with Pip in Editable mode. 
   ```
   make clean
   pip install --verbose --no-build-isolation --editable .
   ```
* Check that the scikit-learn version number ends with `.dev0` 
   ```
   python -c "import sklearn; sklearn.show_versions()"
   ```
* Install development dependencies: `pip install pytest pytest-cov flake8 mypy numpydoc black==22.3.0`
* Add the upstream remote: `git remote add upstream https://github.com/scikit-learn/scikit-learn.git` 
* Check that the `upstream` and `origin` remotes are configured correctly by running `git remote -v` 
   * `upstream` is the alias for the sklearn repo 
   * `origin` is the alias for your fork of the repo 
* Synchronize your `main` branch with the `upstream/main` branch
   ```
   git checkout main 
   git fetch upstream 
   git merge upstream/main 
   ```
* (Optional) Install pre-commmit hooks
   ```
   pip install pre-commit 
   pre-commit install 
   ```

### Working on an issue 
* Create a branch for your changes: `git checkout -b my_feature` 
* Make changes, then `add` and `commit` files: 
   ```
   git add some_file 
   git commit -m "message" 
   ```
* Push changes to your GitHub fork: `git push -u origin my_feature` 
* "You will have to run the `pip install --no-build-isolation --editable .` command every time the source code of a Cython file is updated (ending in .pyx or .pxd). Use the --no-build-isolation flag to avoid compiling the whole project each time, only the files you have modified." 
* Periodically synchronize your branch with the `upstream/main` branch, to pull in any changes that have been made to scikit-learn while you have been working on your branch. 

### Getting your changes accepted

* To update your code based on feedback, make changes locally, then push to your fork. 


https://scikit-learn.org/stable/developers/contributing.html

* This is the scikit-learn project repository: https://github.com/scikit-learn/scikit-learn.
   * To contribute, fork this repository. 
* My fork of scikit-learn: https://github.com/mdhornstein/scikit-learn-github-tutorial
* Clone the fork locally to disk: 
   ```
   git clone https://github.com/mdhornstein/scikit-learn-github-tutorial
   ```
* Update conda: `conda update conda`

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


# Contributing to MatplotlibDeprecationWarnings issue 24797

The issue is here: https://github.com/scikit-learn/scikit-learn/issues/24797.  

* "Contributors willing to address this issue, please offer one example per pull request."
* I will use my local conda environment `sklearn-dev`. 
* "Also be sure to install matplotlib 3.6.1 locally in order to reproduce the Warning."
  * My sklearn-dev environment does not have matplotlib. So I need to install a specific version of matplotlib. 
  * This reference shows how to install matplotlib: https://anaconda.org/conda-forge/matplotlib
  * I need to run: `conda install -c conda-forge matplotlib=3.6.1` 
  * Output is here: https://gist.github.com/mdhornstein/32e0138bc292313e3f98ab4cc24705e7
* Generated a GitHub personal access token in Settings then Developer Settings. 
* It appears that my matplotlib version is incorrect: 
  ```
  (sklearn-dev) na@Nas-MacBook-Pro scikit-learn-github-tutorial % python
  Python 3.8.5 (default, Sep  4 2020, 02:22:02) 
  [Clang 10.0.0 ] :: Anaconda, Inc. on darwin
  Type "help", "copyright", "credits" or "license" for more information.
  >>> import matplotlib
  >>> matplotlib.__version__
  '3.3.2'
  ```
* We can use `conda list` to see a list of packages installed (see reference [here](https://docs.conda.io/projects/conda/en/latest/commands/list.html)). The format of the printout is as follows: 
  ```
  (sklearn-dev) na@Nas-MacBook-Pro scikit-learn-github-tutorial % conda list
  # packages in environment at /Users/na/opt/anaconda3/envs/sklearn-dev:
  #
  # Name                    Version                   Build  Channel
  alabaster                 0.7.12                   pypi_0    pypi
  attrs                     22.1.0             pyh71513ae_1    conda-forge
  ```
* We can look specifically for the version of matplotlib: 
  ```
  (sklearn-dev) na@Nas-MacBook-Pro scikit-learn-github-tutorial % conda list | grep matplotlib
  matplotlib                3.6.1           py310h2ec42d9_1    conda-forge
  matplotlib-base           3.6.1           py310he725631_1    conda-forge
  ```
