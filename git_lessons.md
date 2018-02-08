# A Rare Monument

A Text Adventure Game by the VH Bros

## Git Lessons

### Lesson 1 | VS Code Integrated Terminal and Git setup

- [ ] Open VS Code
- [ ] Type ``` ctrl+` ```
  - [ ] Expected response: This should cause a terminal to open at the bottom of your screen
- [ ] In the terminal type ``` git --version ```
  - [ ] Expected response: ``` # git version 2.7.4 ```
- [ ] Type ``` git config --global user.name "Your Name" ```
- [ ] Type ``` git config --global user.email your.email@example.com ```
- [ ] Now type ``` git status ```
  - [ ] Expected response: 

```
On branch master
Your branch is up-to-date with 'origin/master'.
```

Congratulations! Git is set up and ready to track any changes made to this directory. Now we just need to learn how to properly switch to a different branch, make changes and additions, save the changes and merge the branch back into the master branch.

### Lesson 2 | Creating New Files

This lesson will teach some new git commands, as well as some helpful things to know about your new fancy text editor VS Code.

- [ ] Let's start by creating a new file. Let's call it ``` brainstorm.md ```.
  - [ ] In VS Code press ``` ctrl ```+``` n ```. This should cause a new file to open in your editor labeled ``` Untitled-1 ```
  - [ ] Before we do anything else, let's name it. When naming our files the code extension provides special helpful highlighting, so naming it before typing gives us this ability from the start. Press ``` ctrl ```+``` shift ```+``` s ```. This is the save-as keyboard shortcut.
  - [ ] A screen pops up, in this screen name your document ``` brainstorm.md ```.
- [ ] At the top of the file ad the following code:

```md
# A Rare Monument

A Text Adventure Game by the VH Bros

## Brainstorms
```

The above is referred to as markdown. It's a simple language that gets converted into html on a website. We use it for a few files because it is easy to learn and write because it looks just like a lot of Word Processors. We'll learn more about what the ``` # ``` and ``` ## ``` means later.

Congratulations! You created a new markdown file named brainstorm, and added some markdown to it so we know how to use it. We will use this file to add different brainstormed ideas for our game!

### Lesson 3 | Commiting Your Changes