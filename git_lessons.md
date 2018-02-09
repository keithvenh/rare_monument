# A Rare Monument

A Text Adventure Game by the VH Bros

## Git Lessons

### Lesson 1 | VS Code Integrated Terminal and Git setup

- [ ] Open VS Code
- [ ] Type ``` ctrl+` ```
  - [ ] Expected response: This should cause a terminal to open at the bottom of your screen
- [ ] In the terminal type ``` git --version ```
  - [ ] Expected response: ``` git version 2.7.4 ```
- [ ] Type ``` git config --global user.name "Your Name" ```
- [ ] Type ``` git config --global user.email your.email@example.com ```
- [ ] Now type ``` git status ```
  - [ ] Expected response: 

```bash
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commmit, working directory clean
```

Congratulations! Git is set up and ready to track any changes made to this directory. Now we just need to learn how to properly switch to a different branch, make changes and additions, save the changes and merge the branch back into the master branch.

### Lesson 2 | Creating New Files

This lesson will teach some new git commands, as well as some helpful things to know about your new fancy text editor VS Code.

- [ ] Let's start by creating a new file. Let's call it ``` brainstorm.md ```.
  - [ ] In VS Code press ``` ctrl ```+``` n ```. This should cause a new file to open in your editor labeled ``` Untitled-1 ```
  - [ ] Before we do anything else, let's name it. When naming our files the code extension provides special helpful highlighting, so naming it before typing gives us this ability from the start. Press ``` ctrl ```+``` shift ```+``` s ```. This is the save-as keyboard shortcut.
  - [ ] A screen pops up, in this screen name your document ``` brainstorm.md ```.
- [ ] At the top of the file ad the following code:

```markdown
 1 # A Rare Monument
 2 
 3 A Text Adventure Game by the VH Bros
 4 
 5 ## Brainstorms
```

The above is referred to as markdown. It's a simple language that gets converted into html on a website. We use it for a few files because it is easy to learn and write because it looks just like a lot of Word Processors. We'll learn more about what the ``` # ``` and ``` ## ``` means later.

Congratulations! You created a new markdown file named brainstorm, and added some markdown to it so we know how to use it. We will use this file to add different brainstormed ideas for our game!

### Lesson 3 | Commiting Your Changes

Okay, so you've added a file and made some changes to the file in our git repository. But how do you save those changes? And how to you get those changes to sync up to the remote repository hosted online. This is the magic of git.

- [ ] In your terminal, type ``` git status ```

Your response should look something like this:

```bash
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        brainstorm.md

no changes added to commit (use "git add" and/or "git commit -a")
```

This is git telling you that you have a new file that you have created, but you haven't told git to track the changes you make to that file.

- [ ] To add *all* files so that git will track them, simply type ``` git add . ``` (The ``` . ``` here simply means everything in the current working directory).
- [ ] Now, type ``` git status ``` again.

Your response should look like this:

```bash
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   brainstorm.md
```

We now see that our new file is ready to be committed. In git, committing is fairly similary to saving changes. However, git remembers each commit made, so that if you ever change a bunch of things, but don't like the changes, you can tell git to go back to a time before you made those changes, and all your files will look exactly as if you had never made those changes in the first place. The power of git is that it is version control, allowing you to recover to any point in the process. The recovery points are where you made commits. So, lets commit these changes so that we can come back to this point if we have any issues. 

The git commit command is simple, but it requires a parameter, a message. This message describes the changes you made to the repository, so that it is easy to tell what everyone else has been doing, and easy to tell where something went wrong if that happens.

- [ ] In your terminal type ``` git commit -am "Add brainstorm file" ```
  - [ ] Commit messages are usually typed in present imperative like above rather than past like "Added brainstorm file". Don't ask me why, its just a convention.
- [ ] Now, type ``` git status ``` again.

Your response should resemble:

```bash
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working directory clean
```

This is telling us that we have a commit on our local computer that isn't on the remote computer. To add all of our commits on our local computer we are going to ``` push ``` our changes to the remote origin.

- [ ] In your terminal, type ``` git push ```

Your response shoud be something like:

```bash
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.21 KiB | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To git@github.com:keithvenh/rare_monument.git
   050b4ff..6b8fc90  master -> master
```

- [ ] Now type ``` git status ``` again:

```bash
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
```

And we see that we are up-to-date. Meaning that our computer matches the remote.

To summarize the process:

1. You modify a file or create a new file.
2. These new or modified files are called "Untracked" or "Unstaged".
3. You use ``` git add . ``` to track and stage the files.
4. The files are now staged, which means ready to be commited.
5. You use ``` git commit -am "Some Message" ``` to commit your changes to the local repository.
6. Your local repository is now out-of-sync with the remote repository.
7. You use ``` git push ``` to push your changes to the remote repository.
8. Now your local repository is back in-sync with the remote repository and you are ready to do it all over again.

- [ ] Practice the above process again by creating a new file called ``` tasks.md ```

Congratulations, you are well on your way to becoming a **git guru**

### Lesson 4 | Branching

One last git lesson to make you just dangerous enough to break everything: Branching. Up to this point we have been working on the 'master' branch. This is the part of the code that our program is going to run on. But lets say our program is good to go, but now we want to add a feature. Well, we want to develop this feature over time, committing our changes as we usually do, but if we were to commit our changes to the master branch, it would completely change the program. This is where branching comes in. Each time we begin to work on a new feature, we need to create a new feature branch so that we can develop the feature over time. Then, when the feature is done, and working well, we can merge it back into the master branch. 

Now, when you originally branch, your branch looks identical to the master branch. But as you make changes and commits to your branch, the master branch doesn't change, only your feature branch does. Then, when you are ready for your program to look like your feature branch you merge it back into master, causing master to look identical to your feature branch.

Branching is a good habit to get into, even in the early stages when there isn't much to break, so let's see how it works now.

We want to create a messaging feature, so that we can type more detailed messages back and forth to each other regarding app development. So lets create a message branch.

- [ ] In your terminal type ``` git checkout -b Messages ```

Response:

```bash
Switched to a new branch 'Messages'
```

In this command you are checking out a new branch with ``` checkout ```. You are creating a new branch if one by the name of 'Messages' doesn't already exist iwth ``` -b ```. And you are naming the branch ``` Messages ```. And as the response of the terminal suggests, you have switched to a new branch.

Now, let's quickly add the message feature.

- [ ] Create a new document called ``` messages.txt ``` (remember ``` ctrl ``` + ``` n ``` and ``` ctrl ``` + ``` shift ``` + ``` s ```).
- [ ] In the messages.txt document type:

```txt
Your Name: Hey, I created this message document so that we could type longer messages to each other if there is something that we need to report on.
```

- [ ] Now, go through the git steps of tracking, adding and commiting your changes. Here are the commands if you can't remember:
  - [ ] ``` git add . ```
  - [ ] ``` git commit -am "YOUR MESSAGE" ```
- [ ] Now, we can push this branch up to the remote repository by using ``` git push origin Messages ```
- [ ] Great, now that we have finished the message feature we are going to merge it back into the master branch.
- [ ] Type ``` git checkout master ```

```bash
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'
```

- [ ] Type ``` git merge Messages ```
- [ ] The branches have been merged, now we commit our changes again with ``` git commit -am "YOUR MESSAGE"
- [ ] If we are sure that we are done with the Message branch we can delete it, type ``` git branch -d Messages ```
- [ ] Now we push all our changes up to the remote repository with ``` git push ```

Congratulations! You have successfully created a new feature branch with ``` git checkout -b BrancName ```. You have made changes to that branch and pushed it up to the remote repository. You have merged the branch back into master by first checking out master with ``` git checkout master ``` and then using ``` git merge BranchName ```. Next you commited the changes to the master branch, deleted the old branch with ``` git branch -d BranchName ``` and then pushed the up=to-date local repository to the remote repository.

You've come a long way, and it is likely very overwhelming what you have just learned, but as you use your commands, over time it will become second nature. Let's move on to the final git lesson: Process.

### Lesson 5 | The Git Process

Now, technically, there is no right or wrong way to use git. You can make a commit every time you save a file, or you can use it every time you get up to get a snack. But while there is no right or wrong way, there is a way that makes the most sense.

Here are some guidelines for when you should make git commits and pushes:

- [ ] Everytime you sit down to start working, type ``` git status ``` This should tell you if your branch is up-to-date with the remote repo.
- [ ] If your branch is ahead of the remote repo, you should use ``` git push ``` to push your changes to the remote. And then use ``` git pull ``` to get any changes that were on the remote that weren't on your local computer.
- [ ] If your branch is behing of the remote repo, you should use ``` git pull ``` to pull all the changes from the remote down to your computer.

Now we are certain that you are starting with an up-to-date copy of the repo! Now what? When do we make out commits and our pushes?

- [ ] Anytime you finish what you would say is a large self-contained section, I would recommend making a commit.
  - For example, I made a commmit every time I finished one lesson. I had completed a self-contained section that was easy to wrap my mind around. It also makes it easy to write the message for the commit this way "Finish Lesson 1" for example.
- [ ] Anytime you were working on a particularly hard bit that causes you to give a sigh of relief that it is finished is a good time to make a commit.
- [ ] Anytime you fix some bugs, glitches or typos, its a good time to make a commit with the "Bug Fixes" message.
- [ ] Anytime you are ready to 'call it a day' you should make a commit.

These are the most common and most sensible time to make commits, but if you start to think, man, I've done a lot, you may want to just commit right in the middle of something you are working on. Just like savind a Word document.

- [ ] Lastly, everytime you wrap up a branch you should commit your changes and push them to the remote repo with ``` git push ```
- [ ] In addition, anytime you are ready to 'call it a day' you should push the changes to the ``` remote repo ```.

This last point is most important because it allows everyone else working on the project to grab the most up-to-date version whenever they decide to sit down and start working on a project.

Thats all there is to it. You now know how to do most of what is necessary in git. There is still more to learn, but these few basic commands are what you will need to get by on a regular basis. Everything else can be looked up with a simple Google search.

Below is a table of all the commands we covered over that last 5 lessons, and what they do.

| Command | Result |
| ------- | ------ |
| ``` git add . ``` | Add files to be tracked and staged |
| ``` git commit -am "Message" ``` | Commit changes to local repository |
| ``` git push ``` | Send changes to your remote repository |
| ``` git status ``` | List all changed and new files |
| ``` git checkout -b BranchName ``` | Create a new branch and switch to it |
| ``` git checkout BranchName ``` | Switch between branches |
| ``` git branch ``` | List all of the branches |
| ``` git branch -d BranchName ``` | Delete the feature branch |
| ``` git push origin BranchName ``` | Push the branch to the remote repository |
| ``` git merge BranchName ``` | Merge the feature branch into your active branch |
| ``` git pull `` | Fetch and merge changes from the remote repository to your local computer |

Onward and Upward!