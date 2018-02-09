# A Rare Monument

A Text Adventure Game by the VH Bros

## Git Lessons

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

[DIRECTORY](README.md) | [LESSON 3](03-lesson_three.md) | [LESSON 5](05-lesson_five.md)