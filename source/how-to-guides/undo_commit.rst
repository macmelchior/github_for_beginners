#####################
Undo your last commit
#####################

You can undo the last commit you made while keeping or discarding the changes.
The method depends on whether you already pushed your commit to a remote repository like GitHub.


**What you'll need**

   * `Git <https://git-scm.com/>`_ versioning system.
   * A repository with at least one commit.


Revert a commit that has not been pushed
========================================

The ``git reset`` command is the primary way to undo changes that you have not pushed to a remote repository. 

1. Open the terminal and navigate to your local repository using ``cd`` command.
2. Use ``git reset <flag> HEAD~`` with appropriate flag.
   
    .. list-table::
      :header-rows: 1
      :widths: 20 40 40

      * - Flag
        - Effect
        - When to use
      * - ``--soft``
        - Keeps changes staged.
        - You want to reword the commit or add more files.
      * - ``--mixed``
        - Keeps changes, unstages them.
        - Undo the commit while keeping your changes ready to re-commit.
      * - ``--hard``
        - Discards all changes.
        - Revert the commit and wipe the changes it introduced.
    
    .. warning::

        ``git reset --hard HEAD~`` permanently deletes your uncommitted changes. 
        The edits are removed from your disk and cannot be recovered using Git.

Revert a pushed commit
======================

If you've already pushed your commits to a remote repository

1. Open the terminal.
2. Enter ``git revert HEAD`` and edit the commit message. This will return your local repository to the state before the last commit.
3. Push the commit. Use ``git push`` command. After this, changes from the last commit are reverted.