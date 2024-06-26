---
tags: kids, git, catch-up
languages: git
type: catch-up
---

##Putting Code Online

So you do a lab, and then you spill water all over your laptop and fry it. It's the modern day version of "my dog ate my homework". Good thing the tech industry has thought of that. 

So far, we've been using Github just to take labs from the cloud and bring them down to our ocmputers to work on them, but the real power of github comes in the form of version control and hosting your code in the cloud. Version control means the ability to save snapshots of your work over time so that you can go back to different snapshots if you mess something up down the line. We can push these snapshots (called commits) to github so that they can be accessed from anywhere, allowing for collaboration with other developers.


###What is GIT?

First of all, it’s important to note that git and github aren’t the same thing. Github is where we save our code in the cloud, while git is a version control system that lives on your computer. You use git from the command line, like when you cloned a lab to your computer using `git clone`


###Git with Github
We use the Git in order to host our code on Github.

Let's say you work on a lab, and get half of the tests passing, but then you have to go home for the day. But there's a risk you could drop your laptop in the Hudson river on the way home and you'd lose all your work. So besides emailing it to yourself, which is incredibly tedious, how could you easily save your code?


The best way to save your work it to put it on Github in a repository. So how do we get it there?

Go ahead and fork this repository. (Head to the top of this page, click the fork icon, fork this lab in Github and then clone it down).
Once you're inside the directory of this lesson, go ahead and make a new file called `learning.md`. In the file, type "Hello world!" save the your changes.

Now, in terminal in the directory of this lesson, enter `git status`. You should see something like this:

![IMAGE](git_status.png)

Git is telling us that we have added a file to our directory, but it also says our changes haven't been tracked yet. Git is smart enough to know we've added a file, but this file and the contents of the file aren't yet set to head up to the cloud.

We have to individually add files to Git by entering in terminal `git add name_of_file`. In this case, we'd type `git add learning.md`. We don't get any feedback from git, which means our file was successfully added. If we type `git status` again, we see:

![IMAGE](git_add.png)

Now we see the line `Changes to be committed:`. So far all we've done is added a file, which is like telling Git, yes please keep track of these specific changes. In order to actually save the changes, we have to commit them. A commit is like taking a snapshot of your entire codebase at a moment in time. Commiting often is a really great workflow because you can always rewind in time to different snapshots if you ever break your down the road.

To commit, we type `git commit -m "enter a message here`. The `-m` stands for message, which is what gets passed in quotation marks. This is a commit message. A commit message is a description of the work that you've done that accompanies the snapshot. Commit messages are really helpful because future you can look at the messages and understand exactly what work you did on your code.

Once you enter your commit, you should see `On branch master Your branch is up-to-date with 'origin/master'.` This means your changes have been succesfully committed and a snapshot of your code was taken.

So now it's time to put your code on Github. We have to push the code up there with `git push`. Which actually sends the code to Github. Now, if you go to Github in the browser to this repository and refresh the page, you should see `learning.md` up there!

So heres's a summary of that workflow:

* git add file_name
* git commit -m "commit message"
* git push