# Contributing to GitWiki

[What to work on?](##What-to-work-on)

[Issues](##Issues)

[Workflow](##Workflow)

[License](##License)

## What to work on

Know anything about git? Want to add-on to a section that already exists? Learning something and want to write about that? Notice an error somewhere?

There's no one way to contribute, no specific thing you have to work on. If a topic you want to work on already has a section created: see if there's something you can do to add onto it. If it hasn't: feel free to make that new thing.

## Issues

[Issues](https://github.com/larkceresin/GitWiki/issues) will have a mixture of missing sections and other types of issues needing to be fixed on things that exist. This can be missing information, grammatical errors, or formatting issues among others.

Everyone is open to make a [new issue](https://github.com/larkceresin/GitWiki/issues/new) if they notice an issue somewhere or have additional content they know of that should be added (even if they personally don't want to write it)

## Workflow

The following process is the best way to contribute to the project:

1. [Fork](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) the project. This creates your own local copy of the repo that you can work in.
2. Clone your fork (to where you'll be working) and configure a remote to connect back to the main repo
    ```bash
    # clone your repo
    git clone https://github.com/<your-username>/GitWiki
    # navigate to the new directory
    cd GitWiki
    # Assign original repo to a remote. We're calling it 'upstream'
    git remote add upstream https://github.com/larkceresin/GitWiki
    ```
3. If it's been a while since you've cloned, you'll want to pull any changes from the original repo.
    ```bash
    git checkout main
    git pull upstream main
    ```
4. Before starting, comment on an issue (so you can be assigned to it) or open a new issue and leave a comment that you'll work on it. This will allow less conflict with multiple people working on the same thing. For each new part you're working on: work in a new branch.
    ```bash
    # to create and move to a new branch at the same time
    git checkout -b <branch-name>
    # to just create a new branch
    git branch <branch-name>
    # to switch to a branch that already exists
    git checkout <branch-name>
    ```
5. You can start writing / editing! If you're creating a new section it's suggested to use the [template](./template.md) for a general layout to get started. You can add additional sections as you see fit. 

6. Stage, commit, and push your changes to your forked repo.
    ```bash
    # stage changes
    git add <parameters of what you want to stage>
    # create a commit message in the same line
    git commit -m "<commit message here>"
    # push commited content to your fork
    git push origin <branch-name>
    # you may be notified to set-upstream for the branch you're pushing to. Follow instructions in terminal
    ```
7. Open a [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests). Try to be clear about what you worked on.
    * you might get comments on your pull request on things that would need to be fixed before being merged to the main project.

## License
This project is under terms of the [MIT License](./LICENSE)

Please also adhere to the [code of conduct](./code_of_conduct.md)