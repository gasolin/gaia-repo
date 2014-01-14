gaia-repo
=================

Experiment of using repo to manage gaia directories

This repository is part of initiative work to separate gaia module for reuse
https://bugzilla.mozilla.org/show_bug.cgi?id=883711



Download the Repo tool and ensure that it is executable:

    $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    $ chmod a+x ~/bin/repo

Create a dir

    $ mkdir gaiaexp
    $ cd gaiaexp

init repo

    $ repo init -u https://github.com/gasolin/gaia-repo.git
    

or, init repo by branch name, ex: (not exist yet)

    $ repo init -u https://github.com/gasolin/gaia-repo.git -b v1.3


sync repo

    $ repo sync



## For Gaia Developers

Here's howto make your own dev repo settings:

1. Fork https://github.com/gasolin/gaia-repo.git
2. edit default.xml , add a remote to your fork repository, ex:

     <remote name="origin" fetch="https://github.com/gasolin/"/>

3. then sync the project

    $ repo sync


That command will download all required .git for you.


## Contribute

add remote upstream server to keep update

    $ git remote add origin https://github.com/gasolin/gaia.git

run 

    $ sync start <branch name>


## Reference

* Git and repo cheatsheet [http://source.android.com/source/developing.html#git-and-repo-cheatsheet](http://source.android.com/source/developing.html#git-and-repo-cheatsheet)
* Using repo http://source.android.com/source/using-repo.html
* How to build your own 'repo' to Manage project with multiple git repositories  [http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html](http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html)
