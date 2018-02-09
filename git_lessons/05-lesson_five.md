# A Rare Monument

A Text Adventure Game by the VH Bros

## Git Lessons

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

| Command                            | Result                                           |
| :--------------------------------: | ------                                           |
| ``` git add . ```                  | Add files to be tracked and staged               |
| ``` git commit -am "Message" ```   | Commit changes to local repository               |
| ``` git push ```                   | Send changes to your remote repository           |
| ``` git status ```                 | List all changed and new files                   |
| ``` git checkout -b BranchName ``` | Create a new branch and switch to it             |
| ``` git checkout BranchName ```    | Switch between branches                          |
| ``` git branch ```                 | List all of the branches                         |
| ``` git branch -d BranchName ```   | Delete the feature branch                        |
| ``` git push origin BranchName ``` | Push the branch to the remote repository         |
| ``` git merge BranchName ```       | Merge the feature branch into your active branch |
| ``` git pull ```                   | Fetch and merge changes from the remote repository to your local computer |

Onward and Upward!

[DIRECTORY](README.md) | [LESSON 4](04-lesson_four.md) | [MARKDWON LESSONS](../md_lessons/README.md)