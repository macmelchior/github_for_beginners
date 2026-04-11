###############
Getting started
###############

Follow this tutorial to learn basic GitHub workflow.

Introduction
============

In this tutorial, you will learn:

1. How to create a repository.
2. How to create a new branch.
3. How to publish edited file to GitHub.
4. Open a pull request.
5. Merge a pull request.

What you will need:

* `Git <https://git-scm.com/>`_ versioning system.
* A GitHub account.
* `GitHub CLI <https://cli.github.com/>`_.
* Any editor that lets you edit text files. An :abbr:`IDE (Integrated Development Environment)` such as Visual Studio Code is recommended.

Create a repository
============================
First, you need to create a repository. 

1. Create a new project in Visual Studio Code.
2. Press **Ctrl+`**. This will open the terminal at the bottom.
3. In the terminal, enter ``gh repo create``.
4. Select **Create a new repository on github.com from scratch**.
   
   .. image:: _static/gh_repo_create.png
5. Enter repository name.
   
   .. image:: _static/repository_name.png
6. Add a description.

   .. image:: _static/description.png
7. Choose ``Public`` visibility. This will make the repository visible to others.
   
   .. image:: _static/visibility.png
8. Enter ``Y`` to add a **README.md** file.
   
   .. image:: _static/readme.png
9. On next two steps, simply press **Enter** to apply default settings.
   
   .. image:: _static/gitgnore_license.png
10. Enter ``Y`` to confirm creating the repository. You will see a confirmation message.
    
    .. image:: _static/confirm.png
11. Enter ``Y`` to clone the new repository. This will create a copy of the repository on your computer.
    
    .. image:: _static/clone_locally.png

After perfoming the steps, you should see the following file structure:

.. image:: _static/cloned_repo.png


Create a new branch
=============================

Once we have a repository, it is time to create a new branch for our changes.

1. Enter ``git branch`` followed by branch name, for example ``git branch docs-update``.
2. Switch to the branch. Enter ``git checkout docs-update``.
3. Push the branch to GitHub. Enter ``git push -u origin docs-update``


Edit and publish the file
=============================

Once we have a branch for our edits, it is time to edit the ``README.md`` file. Next, we will publish the edited version in our GitHub repository.

1. Open the ``README.md`` file in Visual Studio Code.
2. Edit the file. Add a short description of the repository.
3. Open the command line tool.
4. Enter ``git add README.md``.
5. Enter ``git status`` to make sure that your file is added. You should see something like this: