
###Links

    * http://help.github.com/git-cheat-sheets/
    * http://lea.verou.me/2011/10/easily-keep-gh-pages-in-sync-with-master/

```

git checkout <sha>



git init
git add .

git commit -m "First import"
git commit -a


git status


git branch
git branch -a

git checkout branchname


git co master

git merge xyz            //merge branch xyz with current branch/head

git merge -Xtheirs topbranch
git merge -s ours

git checkout [commit-ref] [filename]

git checkout -b [name of new branch]


git branch -d [name of branch you want to delete]

git branch -D [name of branch you want to delete]



git stash clear
git stash list
git stash apply

git clone /home/alice/project myrepo
git pull /home/bob/myrepo master



git reset --hard ORIG_HEAD

git reflog

git reset --hard HEAD@{6}

```

###version history of a file
```
gitk images/backgroundBG.png
git blame filename
```

###GIT markings
```
<<<<<<< HEAD
=======
>>>>>>> <branchmergedname>
```


###Find commits not available in master and branch

```
git cherry -v <master> <branchname>

Diff3 style conflict
git config --global merge.conflictstyle diff3
```

###Remove stash /discard unstaged changes
```
git clean -df
or
git checkout -- .
```




###Abort/clear Merge action when conflict:
```
git reset --hard HEAD
git reset --merge


git merge and use branch version when conflict:
git merge -Xtheirs develop

```

###Github - fetch changes in parent repo
```
$ git remote add upstream git://github.com/user/origrepo.git
$ git fetch upstream

# then: (like "git pull" which is fetch + merge)
$ git merge upstream/master master

# or, better, replay your local work on top of the fetched branch
# like a "git pull --rebase"
$ git rebase upstream/master
```

###Github Pages

```
git checkout gh-pages // go to the gh-pages branch
git rebase master // bring gh-pages up to date with master
git push origin gh-pages // commit the changes
git checkout master // return to the master branch
```

###To get modified list between two commit
```
git diff --name-only 36d61563 0d1294e
git diff --name-status 36d61563 0d1294e
```

###Export to get all the modified files between two commit in tar file (zip)
```
git diff-tree -r --no-commit-id --name-only --diff-filter=ACMRT $commit_id | xargs tar -rf mytarfile.tar

```