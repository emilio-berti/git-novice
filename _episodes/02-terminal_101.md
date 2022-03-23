---
title: Beginning with the Terminal
teaching: 15
exercises: 0
questions:
- "How do I navigate in command line?"
objectives:
- "Discover the terminal"
- "Use simple commands to navigate your computer in command line"
keypoints:
-   "Use `pwd` to show in which folder you are."
-   "Use `ls` to list the files of a folder"
-   "Use `ls -a` to show **all** files and folders"
-   "Use `cd` to change the folder"
-   "Use `cd ..` to go back one folder"
-   "Use `mkdir` to create a folder"
-   "Use `touch` to create an empty file"
-   "Use `history` to show recent commands"
-   "Use up/down arrows to check latest commands"
-   "Use Ctrl+R to start a reverse search"
---

## What is the Terminal?

> The shell is a program on your computer whose job is to run other programs. Pseudo-synonyms are “terminal”, “command line”, and “console”. There’s a whole StackExchange thread on the differences (What is the difference between Terminal, Console, Shell, and Command Line?), but I don’t find it to be terribly enlightening. Your mileage may vary.

– Jenny Bryan in [*Happy Git with R*](https://happygitwithr.com/shell.html)

The terminal is a command-line program that let you run other programs.

Why would people use command-line rather than **G**raphical **U**ser **I**nterface?
Well one answer is that are more stable that interface, and they tend
to crash less (because they don't have to deal with the graphical part!).
Also some computers, like online servers or high performance clusters,
are almost only accessible through command-line. So it may useful to familiarize
yourself with the shell.

## How can I use it?

If you're on Mac or Linux you should have a program called "Terminal",
if you're on Windows launch the "Git Bash" application.

## Navigating into folders

Once you've launched it you're going to see a black window with a blinking cursor.
Welcome to the terminal!

We're going to go through some basic commands to navigate on your computer.

Because you're navigating into the files and folders of your computer,
it can be useful to know exactly where your are. For this use the `pwd` command
which is short for **p**resent **w**orking **d**irectory. It indicates precisely
where your are.


~~~
$ pwd
~~~
{: .language-bash}

~~~
/c/Users/ke76dimu
~~~
{: .output}

Slashes `/` indicate nested folders. Here (on a Windows computer) it shows that
I am on the `C:/` drive (shorthened in `/c/` here) within the `ke76dimu` Which
is in the `Users` folder.

Whenever you get lost in the command-line, you can always use `pwd` to remind
yourself of where you are.

The **l**i**s**t command `ls` lists the files and folders available in the
specified folder.

~~~
$ ls
~~~
{: .language-bash}

~~~
 Contacts/
 Desktop/
 Documents/
 Downloads/
 Favorites/
 Pictures/
 R/
 Searches/
 Videos/
 Zotero/
~~~
{: .output}

All the names that finish with a slash `/` indicate a folder. Depending on
type of terminal you are using, the folders can also be represented in another
color like in blue.

You can look at what's inside a folder by adding its names after the command:

~~~
$ ls Documents
~~~
{: .language-bash}

~~~
144101.pdf                                  'My Music'@
'AMF_Unikurse_April 2022.pdf'               'My Videos'@
desktop.ini                                 projects/
R/                                          feature_extraction/                         
'WiSe 2021_22_AMF_Unikurse_filled.pdf'      Livres/
Zoom/                                       'Matthias Material'/
~~~
{: .output}

We can see a file `144101.pdf` and many folders (like `R/`) note that folders
with spaces in their names are indicated with single quote ''
like `'Matthias Material'/`.

You can re-check that your working directory hasn't changed by reusing the `pwd`
command.

~~~
$ pwd
~~~
{: .language-bash}

~~~
/c/Users/ke76dimu
~~~
{: .output}

Some files and folders may be special and are not shown by default.
To display them we use the `-a` option of the `ls` command:

~~~
$ ls -a
~~~
{: .language-bash}

~~~
./
../
.atom/
.bash_history
.bash_profile
.bashrc
.gitconfig
.ssh/
.vim/
.viminfo
Contacts/
Desktop/
Documents/
Downloads/
Favorites/
Pictures/
R/
Searches/
Videos/
Zotero/
~~~
{: .output}   

You can now see several files and folders that names begin with a dot `.`
like `.bashrc` and `.vim/`. We're not going to detail their usefulness,
the important thing to remember is that `ls -a` gives you a bigger list of
files, including hidden files.

To change directory we use the **c**hange **d**irectory command `cd`.

Let's say we want to into the `Documents/` folder. We type the `cd` command
followed by the folder name.

~~~
$ cd Documents/
~~~
{: .language-bash}

Recheck where we are with `pwd`

~~~
$ pwd
~~~
{: .language-bash}

~~~
/c/Users/ke76dimu/Documents
~~~
{: .output}



> ## File and Folder names autocompletion
>
> It can become cumbersome to type entire folder names.
> That's why most terminal software offer autocompletion of folder names
> based on typing the beginning of the name then typing the Tabulation (Tab) key
> on the keyboard (The one on the left of the top row of letters on your
> keyboard).
{: .callout}

What about if you want to back in a folder that is the parent of your folder?
Let's say we want to go back where we were instead of the `Documents/` folder.
Well, you can use the special folder name `..` which defines the
**parent folder** of the folder you're in.

~~~
$ cd ..
~~~
{: .language-bash}

~~~
/c/Users/ke76dimu/Documents
~~~
{: .output}

With the terminal we can also create folders with the
**m**a**k**e **dir**irectory command `mkdir`.

~~~
$ mkdir gitintro
$ cd gitintro
$ pwd
~~~
{: .language-bash}

~~~
/c/Users/ke76dimu/Documents/gitintro
~~~
{: .output}

We're also going to use a command to create files easily.
`touch` is a command that let you create empty files to edit them afterwards.

~~~
$ touch terminal-101.txt
$ ls
~~~
{: .language-bash}

~~~
terminal-101.txt
~~~
{: .output}


> ## Recent commands
>
> Use up and down arrows to navigate the latest commands you launched. You can see the last 1,000 commands passed to the terminal using `history`. You can also start a reverse search pressing `Ctrl + R`; start typing to see the latest relevant commands.
{: .callout}