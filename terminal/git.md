Git
===

Merge branch without losing history
-----------------------------------

Rebase your branch on top of the main branch, resolve conflict, and then merge. As you'll have a straight history, you'll be able to fast-forward to merge and this won't create any merge commit.

    git checkout feature
    git rebase main
    # Resolve conflict if there is
    git checkout main
    git merge feature

This and more [from Stackoverflow](http://stackoverflow.com/a/15006856)

Resources:

* [Changing History, or How to Git Pretty](http://justinhileman.info/article/git-pretty/)
* [Better Git configuration](https://hn.premii.com/#/article/14045787)
* [secretGeek: TIL git summary](https://til.secretgeek.net/git/01_summary.html)
* [GitHub Flow Like a Pro](https://haacked.com/archive/2014/07/28/github-flow-aliases/)
