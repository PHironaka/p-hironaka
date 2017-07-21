---
title: Github workflow steps to always follow
date: 2017-05-10 09:50:00 Z
tags:
- github
---

In today's world of Web Development, it's a requirement to have some sort of Git workflow implemented into every project. It's something, I must admit, I'm still getting used to doing. But making good, solid commits is just as important as writing the actual code. Not only for yourself to be able to track progress, but for other developers who might have to work from the same code base. This will be extremely dry, but it's important to always follow these steps:

`git init`. Once you have your work station set up, it's always good practice to run this command.

`git add`. This to add all the code you've generated

`git commit -m "<insert descriptive message>"` Commit your code often, and make sure your description depicts what the commit entails. It doesn't need to be a sonnet, but make it easy for other people to understand what each commit means.

Once you've made a local commit, it's time to visit github.com and create a repository with your Github account.

`git remote add origin <insert github repository link here>`. With you're newly generated repository, this command creates a remote to point your commits and add them to your new github repository.

`git push -u origin master`. Push your commits.

### Workflow once the initial commit has been made:

`git checkout -b <feature you're working on>`. Separate your concerns with different branches. Treat your Master branch as the final staging area. Dont' push code there until it has been vetted.

Once you're satisfied with the updates, repeat `git add .` & `git commit -m "<message>"`.

Next step: `git checkout master`.

Then, make sure to `git merge <name of branch you created those updates on>`, so that your master branch merges properly.

`git push`.

It's that simple.
