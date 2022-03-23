---
title: "Using Git with EVE"
teaching: 15
exercises: 0
questions:
- "How can I use Git with a High-Performance Computer (EVE)?"
objectives:
- "Understand how to synchronize your git project on EVE."
keypoints:
- "Using `git clone` from a project you have on GitHub to synchronize on EVE."
- "Push/pull before making changes to both the EVE and local git directories to avoid conflicts"
- "Alterntively, create a new branch to work on EVE"
---

Working on EVE is not very different than working on your machine, except that you will have to collaborate ... with yourself! Basically, once connected to EVE, you need to clone the remote git repository and keep working as you would do on your machine. However, remember that the git repository on EVE and the one on your laptop are not directly connected, but can communicate only through remote. In other words, if you change something on both the EVE repository and your laptop, when you try to push and pull you will have conflicts. To avoid this, push the changes made on EVE and pull them on your local laptop before start working on your laptop again.

Once connected to EVE, clone the remote repository:

~~~
$ git clone https://github.com/emilio-berti/idiv-git-introduction.git
~~~
{: .language-bash}

~~~
Cloning into 'idiv-git-introduction'...
remote: Enumerating objects: 10049, done.
remote: Counting objects: 100% (1492/1492), done.
remote: Compressing objects: 100% (715/715), done.
remote: Total 10049 (delta 926), reused 1246 (delta 775), pack-reused 8557
Receiving objects: 100% (10049/10049), 22.61 MiB | 10.21 MiB/s, done.
Resolving deltas: 100% (6211/6211), done.
~~~
{: .output}

Move into the new cloned directory, and check the branch you're in:

~~~
cd idiv-git-introduction/
git status
~~~
{: .language-bash}

~~~
On branch gh-pages
Your branch is up to date with 'origin/gh-pages'.

nothing to commit, working tree clean
~~~
{: .output}

An alternative to avoid conflicts is to create another branch specific for EVE. As scripts to submit jobs and paths within files are specific to the HPC, it may also be better to switch to a new branch instead of working on the main branch. Switch to a new branch called `HPC`:

~~~
git checkout -b HPC
~~~
{: .language-bash}

And check again which branch you're in:

~~~
On branch HPC
nothing to commit, working tree clean
~~~
{: .output}
