# gitforscience-sandbox

Sandbox for Git-for-Science Workshop.

## Overleaf document

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

Make your repo identical to the overleaf repo. Be careful with this ... you will loose everything in the master branch:

    $ git reset --hard overleaf/master
    # push it to your remote
    $ git push --force

## Update Overleaf document with local changes

Edit your Overleaf document locally:

    $ atom main.tex  # choose your favorite LaTeX editor

Commit your changes:

     
