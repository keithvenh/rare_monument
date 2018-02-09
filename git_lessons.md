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
