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

## Exercise 1 - Pull down a repository
## Exercise 2 - Create a branch
## Exercise 3 - Make updates to your branch
## Exercise 4 - Create a Pull Request


# Exercise 1 - Pull down a repository
** Ensure you have Git installed

Follow the steps and complete the exercise.
1. Navigate to our practice repository at [https://github.com/BlockVestment/github-practice](https://github.com/BlockVestment/github-practice)
2. Find the green **Code** button and click on it.  Click over to HTTPS and copy the URL.
3. Locate a Folder on your computer where you would like to download the repository to (example: `../Coding/BlockVestment`)
4. If you are using VSCode, Go to File > Open and select the Folder from above.
5. In VSCode, Go to Terminal > New Terminal
6. In the Terminal, type `git clone <paste the github url we copied>`
== Pause ==
What is happening?  You are telling Git, hey clone this repository for me. It will look for information in the .git and pull down everything in the repository to your local machine.
== Unpause
7. Confirm that a new folder `github-practice` has been downloaded locally