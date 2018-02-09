# A Rare Monument

A Text Adventure Game by the VH Bros

## Git Lessons

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

[GO TO LESSON 4](lesson_four.md)