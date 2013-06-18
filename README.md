gaia-repo
=================

Experiment of using repo to manage gaia directories

Create a dir

    $ mkdir gaia
    $ cd gaia

init repo

    $ repo init -u https://github.com/gasolin/gaia-repo.git

init repo by branch name, ex: (not exist yet)

    $ repo init -u https://github.com/gasolin/gaia-repo.git -b v1.0.1


sync repo

    $ repo sync



## For Gaia Developers

Here's howto make your own dev repo settings:

1. Fork https://github.com/gasolin/gaia-repo.git
2. edit default.xml , add a remote to your repository, ex:

     <remote name="gasolin" fetch="https://github.com/gasolin/"/>

  2.1 replace `project remote="gaia"` to `project remote="<your name>"`, ex:

      <project remote="gasolin" name="gaia" path="."/>


3. then sync the project

    $ repo sync


That command will download all required .git for you.

## Reference

* Git and repo cheatsheet [http://source.android.com/source/developing.html#git-and-repo-cheatsheet](http://source.android.com/source/developing.html#git-and-repo-cheatsheet)
* How to build your own 'repo' to Manage project with multiple git repositories  [http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html](http://blog.gasolin.idv.tw/2013/05/how-to-build-your-own-repo-to-manage.html)