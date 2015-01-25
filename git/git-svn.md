###Links

* http://www.viget.com/extend/effectively-using-git-with-subversion/
* http://flavio.castelli.name/howto_use_git_with_svn
* http://justaddwater.dk/2009/03/09/using-git-for-svn-repositories-workflow/
* http://stackoverflow.com/questions/4394288/why-does-git-svn-init-create-an-empty-repository
* http://brandon.dimcheff.com/2009/01/04/commit-a-linear-git-history-to-subversion.html


###Git-SVN
```
git svn clone -s [url_to_svn_repository] [project_name]
git branch -a #show all branches local(git) and remote(svn)

git status

git svn info #show svn details (also URL)

#create local Git branch that mirrors remote svn branch

git checkout -b local/RELEASE-0.12 RELEASE-0.12 #will connect with a remote svn branch named ‘RELEASE-0.12′

git svn dcommit –dry-run # -n will show which svn branch you will commit into:

#=> Committing to http://svn.edgewall.org/repos/trac/branches/0.11-stable …

git svn rebase # pull changes from svn repository

git svn dcommit # push your local git commits to svn repository

```


###SourceTree log

```
git -c diff.mnemonicprefix=false -c core.quotepath=false -c credential.helper=sourcetree fetch origin 

git -c diff.mnemonicprefix=false -c core.quotepath=false -c credential.helper=sourcetree svn fetch 

git -c diff.mnemonicprefix=false -c core.quotepath=false -c credential.helper=sourcetree push -v --tags origin master:master 

git pull --rebase origin master

```

###Get modified files only

```
git archive --output=<file> HEAD $(git diff --name-only ...)

tar -czf <file> $(git diff --name-only ...)

cp $(git diff --name-only ...) <export-directory>

````


