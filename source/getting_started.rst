###############
Getting started
###############

Follow this tutorial to learn basic how to publish your project on GitHub.

Introduction
============

In this tutorial, you will learn:

1. How to create a repository.
2. How to create a new branch.
3. How to publish an edited file to GitHub.
4. Open a pull request.
5. Merge a pull request.

We will perform all these steps in a terminal.

What you will need:

* `Git <https://git-scm.com/>`_ versioning system.
* A GitHub account.
* `GitHub CLI <https://cli.github.com/>`_.
* Any editor that lets you edit text files. An :abbr:`IDE (Integrated Development Environment)` such as Visual Studio Code is recommended.

Create a repository
============================
First, you need to create a repository.

1. Create a new project in Visual Studio Code.
2. Press ``Ctrl+```. This will open the terminal at the bottom.
3. In the terminal, enter ``gh repo create``. This will open an interactive repository creator.
4. Select ``Create a new repository on github.com from scratch``.
5. Next, enter repository name.
6. Add a description.
7. Choose ``Public`` visibility. This will make the repository visible to others.
8. Enter ``Y`` to add a ``README.md`` file. This will be our first file on GitHub.
9. On the next two steps, simply press **Enter** to apply default settings.
10. After that, enter ``Y`` to confirm creating the repository. 
    You will see a confirmation message similar to this:
   
   .. code-block:: console
   
      ? This will create "docs-update" as a public repository on github.com. Continue? Yes                                                                                                                                                                                                          
      ✓ Created repository macmelchior/docs-update on github.com
      https://github.com/macmelchior/docs-update

11. Enter ``Y`` to clone the new repository. This will create a copy of the repository on your computer.
12. You should see the following file structure:

    .. image:: _static/cloned_repo.png


Create a new branch
=============================

Once you have a repository, it is time to create a new branch for your changes.

1. Enter ``git branch`` followed by branch name, for example **docs-update**.
2. Switch to the branch. Enter ``git checkout docs-update``.
3. Push the branch to GitHub. Enter ``git push origin docs-update``.


Edit and publish the file
=============================

Once you have a branch, you can start editing the ``README.md`` file. 
Next, you will publish the edited version in your GitHub repository.

1. Open the ``README.md`` file in Visual Studio Code.
2. Edit the file. Add a short description of the repository.
3. Open the terminal.
4. Enter ``git add README.md``.
5. Enter ``git status`` to make sure that your file is added. You should see something like this:
   
   .. code-block:: console
      
      Changes to be committed:
         (use "git restore --staged <file>..." to unstage)
            new file: README.md
6. Now you have to commit your edited file. Enter ``git commit``.
7. ``COMMIT_EDITMSG`` file will open. Enter the commit message in the window. 
   It can be a short description of the changes.
8. Click **Commit**.
9.  Now it is time to push the file. Enter ``git push origin docs-update``. 
    This will make the file visible on GitHub. To view it, make sure to select correct branch.

Open a pull request
=============================

Once you have a file published in the branch, you should open a **pull request**. 
This will allow the owner of the repository (in this case -- you) to add your changes to the main repository.

1. Enter ``gh pr create``. This will open an interactive creator.
2. Enter the title.
3. Press ``e`` to open a notepad. 
4. Enter the description of changes and close the notepad.
5. Select ``Submit``.
6. You should see a link to the pull request, for example:
   ``https://github.com/macmelchior/github_for_beginners/pull/1``

Merge a pull request
=============================
After a pull request is opened, it needs to be merged with the main branch. 

1. Switch to the main branch. Enter ``git checkout main``.
2. Merge the head branch. Enter ``git merge docs-update``. You should see a summary of changes made on **docs-update** branch:
   
   .. code-block:: console

      Updating 7980fa1..6178f35                                                                                                                                                                                                                                                                   
      Fast-forward
       source/README.md                  | 119 ++++++++++++++++++++++------
3. Push the changes to the main branch. Enter ``git push -u origin main``. You will see a confirmation message. It should end like this:
   
   .. code-block:: console

      branch 'main' set up to track 'origin/main'.

Delete the branch
=============================

After successfully updating the branch, you can delete it.

1. Enter ``git branch -d docs-update``.
2. You will see a confirmation that branch was deleted.

Congratulations! Now you know how to successfully publish your work on GitHub using nothing but console commands.
