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
