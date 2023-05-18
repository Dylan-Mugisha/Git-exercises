# Git exercises
## bundle1
### exercise 1
```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:bundle1 king$ git init
Initialized empty Git repository in /Users/king/Desktop/projects/git exercises/bundle1/.git/
kings-MacBook-Air:bundle1 king$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
kings-MacBook-Air:bundle1 king$ git branch -M main
error: refname refs/heads/master not found
fatal: Branch rename failed
kings-MacBook-Air:bundle1 king$ git checkout -b main
Switched to a new branch 'main'
kings-MacBook-Air:bundle1 king$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        readme.md

nothing added to commit but untracked files present (use "git add" to track)
kings-MacBook-Air:bundle1 king$ git add readme.md
kings-MacBook-Air:bundle1 king$ git commit -m 'first exercises of bundle1'
[main (root-commit) e90a60b] first exercises of bundle1
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
kings-MacBook-Air:bundle1 king$ git remote add origin https://github.com/Dylan-Mugisha/Git-exercises.git
kings-MacBook-Air:bundle1 king$  git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

kings-MacBook-Air:bundle1 king$  git push --set-upstream origin main
Counting objects: 3, done.
Writing objects: 100% (3/3), 225 bytes | 225.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/Dylan-Mugisha/Git-exercises.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
kings-MacBook-Air:bundle1 king$ git checkout -b dev
M       readme.md
Switched to a new branch 'dev'
kings-MacBook-Air:bundle1 king$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/Git-exercises/pull/new/dev
remote: 
To https://github.com/Dylan-Mugisha/Git-exercises.git
 * [new branch]      dev -> dev
kings-MacBook-Air:bundle1 king$ git checkout -b test
M       readme.md
Switched to a new branch 'test'
kings-MacBook-Air:bundle1 king$ git push origin test
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/Git-exercises/pull/new/test
remote: 
To https://github.com/Dylan-Mugisha/Git-exercises.git
 * [new branch]      test -> test
kings-MacBook-Air:bundle1 king$ git branch -D test
error: Cannot delete branch 'test' checked out at '/Users/king/Desktop/projects/git exercises/bundle1'
kings-MacBook-Air:bundle1 king$ git checkout dev
M       readme.md
Switched to branch 'dev'
kings-MacBook-Air:bundle1 king$ git branch -D test
Deleted branch test (was e90a60b).
kings-MacBook-Air:bundle1 king$ git push origin --delete test
To https://github.com/Dylan-Mugisha/Git-exercises.git
 - [deleted]         test
kings-MacBook-Air:bundle1 king$ 
```

### exercises 2
```bash
kings-MacBook-Air:bundle1 king$ # new exercises2 in bundle1
kings-MacBook-Air:bundle1 king$ git add home.html
kings-MacBook-Air:bundle1 king$ git stash
Saved working directory and index state WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git add about.html
kings-MacBook-Air:bundle1 king$ git stash
Saved working directory and index state WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{1}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash
No local changes to save
kings-MacBook-Air:bundle1 king$ git add about.html
kings-MacBook-Air:bundle1 king$ git stash
Saved working directory and index state WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{1}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{2}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git add team.html
kings-MacBook-Air:bundle1 king$ git stash
Saved working directory and index state WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{1}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{2}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{3}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        team.html

Dropped stash@{1} (c5facd25a5a07126997f0b2cd9d214ab5c32c78e)
kings-MacBook-Air:bundle1 king$ git add team.html
kings-MacBook-Air:bundle1 king$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   team.html

kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{1}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{2}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   team.html

Dropped stash@{1} (b8694147191a04c766f6c2015ff372accf2bd7f0)
kings-MacBook-Air:bundle1 king$ git stash list
stash@{0}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
stash@{1}: WIP on dev: 1175418 history in terminal of bundle1-exercises1 added
kings-MacBook-Air:bundle1 king$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html
        new file:   team.html

Dropped stash@{1} (fd7f4875e43e611a797b1a9d484d43752f4173a0)
kings-MacBook-Air:bundle1 king$ git commi -m 'committing changes in ex-2'
git: 'commi' is not a git command. See 'git --help'.

The most similar commands are
        commit
        column
        config
kings-MacBook-Air:bundle1 king$ git commit -m 'committing changes in ex-2'
[dev 39752ab] committing changes in ex-2
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 3 files changed, 36 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 team.html
kings-MacBook-Air:bundle1 king$ git reset --hard
HEAD is now at 39752ab committing changes in ex-2
kings-MacBook-Air:bundle1 king$ git add --all
kings-MacBook-Air:bundle1 king$ 
.
```

## bundle-2 
### exercises 1
```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:bundle1 king$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
kings-MacBook-Air:bundle1 king$ git status
On branch ft/bundle-2
nothing to commit, working tree clean
kings-MacBook-Air:bundle1 king$ git add service.html
kings-MacBook-Air:bundle1 king$ git commit -m 'service.html created'
[ft/bundle-2 8decc70] service.html created
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 service.html
kings-MacBook-Air:bundle1 king$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

kings-MacBook-Air:bundle1 king$  git push --set-upstream origin ft/bundle-2
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 277 bytes | 277.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/Git-exercises/pull/new/ft/bundle-2
remote: 
To https://github.com/Dylan-Mugisha/Git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
kings-MacBook-Air:bundle1 king$ git push --set-upstream origin main
Branch 'main' set up to track remote branch 'main' from 'origin'.
Everything up-to-date
kings-MacBook-Air:bundle1 king$ 
```