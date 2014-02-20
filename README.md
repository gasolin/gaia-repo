gaia-repo
=================

Experiment of using repo to manage gaia directories

This repository is part of initiative work to separate gaia module for reuse
https://bugzilla.mozilla.org/show_bug.cgi?id=883711


## Prerequisites

Download the Repo tool and ensure that it is executable:

    $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    $ chmod a+x ~/bin/repo

Create a dir

    $ mkdir gaia
    $ cd gaia

init repo

    $ repo init -u https://github.com/gasolin/gaia-repo.git


## First time get project

run `sync repo` command to fetch all resources:

    $ repo sync

The first time `repo sync` command is equivalent to `git clone`.
At second run, `repo sync` command is equivalent to `git remote update && git rebase upstream/<branch name>` (refer to [use repo](http://source.android.com/source/using-repo.html) )

add remote upstream server to keep update

    $ git remote add origin https://github.com/mozilla-b2g/gaia.git

and add your gaia origin repository to develop with

    $ git remote add origin https://github.com/gasolin/gaia.git

Now you all set.

## Start developing

To create a new branch to work with, use command 

    $ sync start <branch name> gaia

which is equivalent to `git checkout -b <branch name> upstream/master`.

push your change to your own git

    $ git push origin <branch name>

Then go back to Bugzilla and do all we are already familiar with.

## misc

### init a branch

You can init repo by branch name, ex:

    $ repo init -u https://github.com/gasolin/gaia-repo.git -b v1.3

or change the default branch via command:

    $ repo init -b v1.3

### update specific project

we can use

    $ repo sync <project>

to just update partial code if we've some project other then gaia.


## Reference

* Git and repo cheatsheet [http://source.android.com/source/developing.html#git-and-repo-cheatsheet](http://source.android.com/source/developing.html#git-and-repo-cheatsheet)
* Using repo http://source.android.com/source/using-repo.html
* How to build your own 'repo' to Manage project with multiple git repositories  [http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html](http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html)
