# gitforscience-sandbox

Sandbox for Git-for-Science Workshop.

## Tools

Overleaf:
* https://www.overleaf.com/
* Online collaborative LaTeX editor with integrated real-time preview.
* Uses Git in the background.
* Alternative ShareLatex: https://www.sharelatex.com/

GitHub:
* https://github.com/
* Online service for Git repositories and collaborative developing.

Git:
* https://git-scm.com/
* Version control system for decentralised software development.

LaTex:
* https://www.tug.org/texlive/
* TexLive on macOS: https://www.tug.org/mactex/
* On macOS install it with homebrew: http://yabas.net/blog/install-latex-on-mac-with-brew/
* Write beautiful documents.

Editors:
* Atom: https://atom.io/

Good Alternatives to LaTeX:
* Markdown


## Edit Overleaf document

Read and Edit:
https://www.overleaf.com/15422340tzpscybmktkc

Read only:
https://www.overleaf.com/read/zncknkybdkxg

Git clone:

    $ git clone https://git.overleaf.com/15422340tzpscybmktkc

## Push my Overleaf document to my GitHub repo

Create a Git repo on GitHub and clone it:

    # Please create your own ... just showing the example with my sandbox
    $ git clone git@github.com:cehbrecht/gitforscience-sandbox.git
    $ cd gitforscience-sandbox

Add the overleaf git repo as remote:

    $ git remote add overleaf https://git.overleaf.com/15422340tzpscybmktkc
    $ git remote -v

Make your repo identical to the overleaf repo. Be careful with this ... you will loose everything on your local master branch:

    $ git reset --hard overleaf/master
    # push it to your remote origin master
    $ git push --force

## Update Overleaf document with local changes

Edit your Overleaf document locally:

    $ atom main.tex  # choose your favorite LaTeX editor

Commit your changes:

     $ git status
     $ git commit -a -m "update"
     $ git push

Push your changes to Overleaf:

    $ git pull overleaf master
    $ git push overleaf master

## Merge changes and handle conflicts

First edit Overleaf document and the local document at different sections.
Update your changes with the remote overleaf document. Changes will be merged automatically.

Now make edits at the same text line locally and in overleaf. Update your changes again
but this time you will need to solve a merge conflict.   

## Tag a version

With git you can tag a version:

    $ git tag 0.1
    $ git push --tags

Use this tag to create a release on GitHub:
https://help.github.com/articles/creating-releases/

## Create a DOI to reference your paper

Using an online service you can create automatically a DOI for your paper on GitHub
whenever you make a new release:

https://guides.github.com/activities/citable-code/

## Handle large files with Git

Version controls are made for coding and can handle text files very well.
They can be used for binary files as well but this has some limitations.
You can use Git LFS extension on GitHub to get around these limitations. Large binary files will then be stored in an external storage and not in the Git repo itself. The Git repo has only pointers to these files.

https://git-lfs.github.com/
