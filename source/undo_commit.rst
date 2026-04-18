#####################
Undo your last commit
#####################

You can undo the last commit you made while keeping or disarding the changes.
This is useful when you made a mistake in the code.
The method depends on whether you already pushed your commit. 


.. note::

   ℹ️ **What you'll need**

   * `Git <https://git-scm.com/>`_ versioning system.
   * A repository with at least one commit.


Revert a commit that has not been pushed
========================================

1. Open your local repository in an :abbr:`IDE (Integrated Development Environment)`.
2. Press ``Ctrl+```. This will open the terminal at the bottom.
3. Use one of the following commands:
    ``git reset --soft HEAD~1`` if you want to keep changes from the commit staged. 
    This will just undo the commit while keeping your changes ready to re-commit. 
    ``--soft`` lands you in the state you were in after ``git add`` but before ``git commit``.
    
    ``git reset --mixed HEAD~1`` if you want to keep changes from the commit unstaged. 
    This will undo the commit and unstage the files. You will need to ``git add`` before commiting again.

    ``git reset --hard HEAD~1`` if you want to revert the commit and wipe the changes it introduced.
    
    .. warning::

        This permanently deletes your uncommited changes. 
        The edits are removed from your disk and cannot be recovered using Git.