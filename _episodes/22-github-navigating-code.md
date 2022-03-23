---
title: "Navigating and Searching code on GitHub"
teaching: 25
exercises: 0
questions:
- "How can I use GitHub to navigate my code?"
objectives:
- "Understand key features of GitHub to navigate into the code"
keypoints:
- "Using GitHub commit history allows you to get access directly to your code."
- "You can look at specific files, have them as raw version, or acces their history"
- "It is possible to select a specific line of code to link to it or cite it"
- "Through the settings tab of a project you can collaborators"
- "GitHub issues are a good way to keep track of progress, bugs, and ideas on a project"
---

You can access your last commit on GitHub in a very similar fashion
to `git show`. Find the commit in the top right corner of the repository.

![Locate name of the last commit](../fig/github_commit.png)

Then you can click on it to get the detail of the commit.

![See detail of a commit](../fig/github_commit_detail.png)

Similar to `git log` you can see the history of your commits in the project.

![Locate history of commits of a project](../fig/github_commit_all.png)

If you click on it you see the list of commits of your project.

![History of commits of a project](../fig/github_commit_all_detailed.png)

Through the GitHub interface you can also look at individual files.
For this hover your mouse on a file name and click on it.

![Hover your mouse on a file name](../fig/github_file_selected.png)

Then you can access the file interface of GitHub.

![Detail of a file on GitHub](../fig/github_file_detail.png)

The window is split between the line numbers, the file name, the actual content
of the file and many other features.

One of the most useful one is that you can always access the raw version of
the file which makes it very simple to download.
For that click on the "Raw" button on the top right corner of the file.

![Raw button of file](../fig/github_file_raw.png)

You can also access the commit history of a file by clicking on the history
button in the top right, it will display a list of commits affecting that file.

![Raw button of file](../fig/github_file_history.png)

Through the GitHub interface it is also possible to add collaborators to your
project, so that they can also commit on the repository.
To do that you have first to access the "Settings" tab of your project.

![Settings tab of a GitHub project](../fig/github_settings.png)

Then from there you have to click on "Collaborators" in the menu on the left.
GitHub will ask you to confirm your password for security reasons.

![Collaborators in the settings menu](../fig/github_settings_collaborators.png)

Then click on "add people" to search for people by their GitHub username to add
them to the project.

![Add people to your project](../fig/github_settings_add_people.png)

One additional interesting feature are "GitHub issues". There messages that can
form discussions, and you can track independent bugs and ideas with them.
There are quite commonly used to track the progress (what has been done and
needs to be done) of a project.
