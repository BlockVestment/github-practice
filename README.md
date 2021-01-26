# Getting Started with Git, GitHub, and code repositories

## What is Git?
Git is a software development tool that tracks changes (or history) of our code.  I would describe it as a tree with 2 major pieces: the trunk/base (the trunk where your production code is) and your branches (new features, bug fixes, etc).

The collection of the production code is called a _repository_.

Okay so why do we use Git to track changes in code.  Two major reasons, 
1. Main reason - If our production code breaks, we can roll back to the last working branch because Git remembers the code history.
2. Secondary reason - We can allow multiple developers to work on the same code repository without interfering with other developers.

## What is GitHub?
GitHub is a centralized location to host production code repositories.  You can search for other developers repositories and use their tools/code to solve problems. 

## Installing Git
Go to the [Git download page](https://git-scm.com/downloads) to download Git for either Windows, Mac, or Linux.

## Using Git Branches
We create / use Git Branches to create new features, fix bugs, etc. that we then merge back into our main (production) code through a process called Pull Requests or _PRs_ for short.


# Okay enough theory, let's get some practice with some exercises
This will help you get practice with Git and get experience with the `blockvestment-platform` and `marketing-site` repositories. Woohoo finally!  I'm going to go through the entire process of how I typically write code. I will break this down into 4 exercises, which I will walkthrough with you.

1. Pull down a repository (or a repo)
2. Create a branch and switch to different branches
3. Check status, make updates, add our new updates, and commit our updates to Git history
4. Create a pull request

Ensure you have Git installed for these exercises.

## Exercise 1 - Pull down a repository
These steps will help you pull down a repository

1. Navigate to our practice repository at [https://github.com/BlockVestment/github-practice](https://github.com/BlockVestment/github-practice)
2. Find the green **Code** button and click on it.  Click over to HTTPS and copy the URL.
3. Locate a Folder on your computer where you would like to download the repository to (example: `../Coding/BlockVestment`)
4. If you are using VSCode, Go to File > Open and select the Folder from above.
5. In VSCode, Go to Terminal > New Terminal
6. In the Terminal, type `git clone <paste the github url we copied>`
> == Pause == <br/>
> What is happening?  You are telling Git, hey clone this repository for me. It will look for information in the .git file and pull down everything in the repository to your local machine. <br/>
> == Unpause == 
7. Confirm that a new folder `github-practice` has been downloaded locally

## Exercise 2 - Create a branch
This will be a relatively short exercise as we will be just creating and switching branches.

1. Open up VSCode, If the Terminal is not open go to Terminal > New Terminal.
2. With the Terminal open, type the command `git status` an confirm you are on the `main` branch
> `git status` <br/>
> This command will display the state of the folder you're in aka which files you've updated, changed or deleted. <br/>
> It also gives good information on which Branch you are on.
3. Another way to see which branch you are on is with the command `git branch`
> `git branch` <br/>
> List, create, or delete branches on your local machine.

> Although you can use `git branch` to create branches, I usually only use this command to see which branches I have locally on my machine.
4. From here we want to create a new branch. So type the command `git checkout -b <name of our branch>`
> == Pause == </br>
> The `git checkout` command is a way to switch to different branches that we have locally. When we add the `-b` command, it is telling Git to: **Create our branch and check it out automatically.** </br>
> == Unpause ==
5. From here, type `git status` or `git branch` to confirm we are actually on our newly created branch and NOT on our main branch.

All together the commands should look like this (replace my branch name with whatever you like):
```bash
# confirm the status of local changes
git status
# confirm which branch we are on
git branch
# create a new branch name alexs-branch and switch to it
git checkout -b alexs-branch
# verify the status of local changes or verify the status of which branch we are on
git status OR git branch
```

## Exercise 3 - Make updates to your branch
So this is where we are going to make updates to the branch we just created. Then we are going to add our changed files and commit them to our git history.

1. Open up VSCode in our `github-practice` folder.

2. Check the status of by running the command `git status` to confirm you are on YOUR branch and not the MAIN branch.

3. Open up the `README.md` file and add your name under the section entitled ### **I have completed these exercises** ###. After you add your name let's run the `git status` again.
```bash
git status
```
You will now notice that your file will be highlighted red and say something that looks like this:
```bash
Changes not staged for commit:
modified: README.md
```
> == PAUSE ==<br>
> So you've modified the `README.md` and Git is giving you information: Changes staged for commit. This is telling you that you've made changes AND they have not been added yet.
> <br>== UNPAUSE ==
4. Let's go ahead and add the `README.md` file to our staged files (an intermediary place before we actually commit them to the Git history).
```bash
# Adds the specific file that has changed
git add README.md

# It will add all the changed files
# This is the command I find myself running more often than not
git add .
```
> == PAUSE ==<br>
> So Git is a little strange because there is a two-part process to add modified files to the Git history:<br>
> 1. Adding the files to a staged files state (aka a 'ready' state) **_not added to git history_<br>
> 2. Commiting staged files to git history (aka a 'commit' state)
> <br> == UNPAUSE ==<br>

Let's run `git status` to see these two states:
```bash
# Checks the status (should be green) because we added our files to the 'ready'/'staged' state
git status 
```

5. The next thing to do is commit our staged files to the git history.
```bash
# Commits the staged files to Git history & provide a message/comment about why/which files were changed
git commit -m 'updated README.md'
```
You will see an output saying: <br>
`1 file changed, <some number> additions, <some number> deletions.`<br>
This is saying how many files changed and how many lines of code/changes were either added or removed.

6. When we run `git status` one last time we can confirm that our changes were committed to the Git history.  If all goes well, you should see something like this:
```bash
On branch <name of your branch>
noting to commit, working tree clean
```

## Exercise 4 - Create a Pull Request
This last exercise you will push your updates to the `github-practice` repository, create a Pull Request, and finally merge your code into the main codebase.
1. Open up VSCode in our `github-practice` folder.
2. Run the command `git status` OR `git branch` to confirm you are on YOUR branch and not the MAIN branch.
3. Run

## Putting it all together


# I have completed these exercises: