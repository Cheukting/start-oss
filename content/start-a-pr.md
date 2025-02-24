---
title: "Start making a pull request"
author: "Cheuk"
layout: "single"
summary: "Let's start making a pull request by adding a new project to our list."
showtoc: true
tocopen: true
---

## What is a pull request?

In short creating a pull request (sometimes called merge request, it's the same) is like sending a message to the maintainer. However, to fully understand what is a pull/ merge request, we need to understand what is version control.

### Git and version control

Have you ever modify a document (e.g. homework, essay etc) and would also like to keep the old version so incase you decided you do not like the new change, you can go back to the "previoous save"? You can keep a lot of versions of your document and name it so you remember which one is the latest etc. Or even keep them in different folders if there are more than one files involved.

This situation happens a lot in software development. Developers often need to try new designs and features that may or may not work. To make things more complicated, nowadays we usually work in a team where multiple people may work on the project simultaneously. To keep the project manageable, version control tool is the industry standard used in software development, one such tool is [git](https://git-scm.com/). Although git is not the only version control tool, due to it's popularity, we will by default only explain how to work with git in this workshop.

### What's a commit

A commit is like a checkpoint, a save or a record of your work. It usually have a starting point, where the previous commit is, and all your work and changes since then are recorded in the commit. You can also imagine commits are layers which all combine can bring it up to where the current state of the project is.

It is generally a good idea to make frequent commits so you can have better organization of what changes has been made in which commit. You will also add commit messages to describe what changes you have made in each commit.

Commits are also useful when working in a team as it is easy to see who made certain changes and can ask that person for more information if there are questions. 

### fork, clone, pull, push, merge

The common git operation that you will encounter in OSS contributions are: fork, clone, pull, push, merge. Let's us look at them one by one:

- **fork**: to make a `fork` is to copy a version of the project from the original owners account to your account, your version can diverge from there (if you decided to make independent development from the original) that's why it is called a `fork`
- **clone**: `clone` refers to making a copy from your online account repository (e.g. GitHub repo) to your local machine, we usually keep these two copies the same that's why it is `clone`
- **pull**: to `pull` is to copy the online version (by default the one you `clone` from or otherwise you will have to set in git which online repo you are copying from) and combine with your current local version
- **push**: `push` is the opposite to `pull`, to copy and combine the local version back to the online version
- **merge**: we usually use the term `merge` instead of combine. Instead of seeing as all the work combining together, since all the work are saved as `commit`, which have the relationship of what it came before (and sometime after as well) and that can form `commit` paths, combining `commit`s is like these parths merging together into one.

All these terms may seem scary at first, but don't worry, you will start to understand and get use to it once you start making contributions yourself. Keep this as a reference if you feel a bit lost when starting out.

## Why do we need pull requests in OSS contribution?

Let's come back to pull requests. For those of you who have use git (or other version controls) at work, you may have the question - why do we need to make pull requests and not just push our commits back to the original repo?

Good question! You may not be using pull request at work because everyone in the team are trusted and given direct write access to your work repos. This may not always be the case and sometimes not a good idea in security standpoint. In OSS, since everyone is working in the open and are mostly volunteers, we may not even know each other (that's why code of conduct is important). There need to be a more robust workflow to make sure the contributions are doing good to the open source project rather than harm.

Remember we talked about makeing a `fork`? That's right, at the start of our contribution, we will make a `fork` of the original repo to one that is under our account. Technically, you can do anythink you like (with the license being the limitation) with your own version, however, since you want to contribute back (or sometime called upstreaming) to the original repo, after you made your changes, you will send a pull request to the original repo from the version under your account. 

Once the maintainer received your pull request, they can review your changes and may sometimes request further changes. This is your opportunity to work with others in OSS and learn a lot from them. When the maintainers are happy with your changes, they will accept the changes and merge it into the original repo. Congratulations! You have now contributed to this open source project!

---

## Start making a pull request

I am sure now you are excited to start making a pull request. But before you search for something to work on in your favourite OSS projects, I will kindly invite you to contribute to this project as well. In this website, we collect a list of open source projects that welcome contributions. If there is a project that you think is a good one to contribute to, why don't you add it to this website?

### Step 1 - frok this project

Assuming that you already have a GitHub account (you can [register one](https://github.com/) for free), go to [our GitHub repo](https://github.com/Cheukting/start-oss) and make a `fork`.

### Step 2 - clone to your machine

After forking the project, you'll want a copy on your local machine to start making contributions. Follow the instructions below based on your operating system.

#### For Unix/Linux/macOS:

1. Open your terminal.
2. Use the following command to clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/start-oss.git
   ```
   Replace `YOUR-USERNAME` with your GitHub username.

3. The above command will create a folder `start-oss` with a local copy of the repository. Navigate to the folder:
   ```bash
   cd start-oss
   ```

#### For Windows:

1. Open a terminal (Command Prompt, PowerShell, or Git Bash).
2. Use the following command to clone the repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/start-oss.git
   ```
   Replace `YOUR-USERNAME` with your GitHub username.

3. A folder `start-oss` will be created with a local copy of the repository. Use the following command to navigate into
   the directory:
   ```bash
   cd start-oss
   ```

### Step 3 - add a new project

Open your favourite IDE ([personal recommendation](https://www.jetbrains.com/pycharm/)) and go to `content/projects` create a new file named `YOU-PROJECT.md` (replace `YOU-PROJECT` with the name of the project that you want to add).

In the file, copy and paste this frontmatter:

```aiignore
---
author: "YOUR_NAME"
title: "PROJECT_NAME"
date: "2025-02-01" # date of TODAY
description: "PROJECT_NAME"
tags: ["rust", "python"] # what languages/ technologies this project is using
---
```

After that, add a small description, for example:

```aiignore
PROJECT_NAME is a Python library that can make you code faster.

- [Project repo](LINK_TO_PROJECT_REPO)
- [Contributing docs](LINK_TO_CONTRIBUTING_DOCS)
- [Code of Conduct](LINK_TO_COC)
```

(or you can just copy `content/projects/pyo3.md` and modify)

### Step 4 - (optional) test it locally

Lot of times before you commit your work, you may want to test locally. For this repo, since it is a [Hugo](https://gohugo.io/) website, you may need to [have Hugo installed](https://gohugo.io/installation/) and in the terminal, use the command:

```aiignore
hugo server
```

To run the website locally to check.

### Step 5 - commit your work

After making your changes, you'll need to save them in your local repository by making a commit. Follow the instructions based on your operating system below.

#### For Unix/Linux/macOS:

1. Open your terminal and make sure you are still in the `start-oss` directory:
   ```bash
   cd start-oss
   ```

2. Stage your changes by adding them to the staging area:
   ```bash
   git add .
   ```
   This command will stage all the changes you made. Alternatively, you can specify individual files instead of using
   `.`.

3. Commit your changes with a message:
   ```bash
   git commit -m "Add PROJECT_NAME to the projects list"
   ```
   Replace `"Add PROJECT_NAME to the projects list"` with a relevant description of your changes.

#### For Windows:

1. Open a terminal (Command Prompt, PowerShell, or Git Bash) and navigate to the `start-oss` directory:
   ```bash
   cd start-oss
   ```

2. Stage your changes by adding them to the staging area:
   ```bash
   git add .
   ```
   As mentioned above, this stages all your changes, or you can specify individual files instead.

3. Commit your changes with a message:
   ```bash
   git commit -m "Add PROJECT_NAME to the projects list"
   ```
   Make sure your message reflects the changes you've made.

### Step 6 - push back to GitHub

Now that your changes are committed locally, you need to push them to your forked repository on GitHub. Follow the instructions below based on your operating system.

#### For Unix/Linux/macOS:

1. Make sure you're in the `start-oss` directory:
   ```bash
   cd start-oss
   ```
2. Push your changes to the forked repository on GitHub:
   ```bash
   git push origin YOUR-BRANCH-NAME
   ```
   Replace `YOUR-BRANCH-NAME` with the name of the branch you're working on (by default the branch name is `main` unless you created another branch).

#### For Windows:

1. Open your terminal (Command Prompt, PowerShell, or Git Bash) and navigate to the `start-oss` directory:
   ```bash
   cd start-oss
   ```
2. Push your changes to your forked repository on GitHub:
   ```bash
   git push origin YOUR-BRANCH-NAME
   ```
   Again, replace `YOUR-BRANCH-NAME` with the branch name where you've made your changes (default is `main`). 

### Step 7 - create pull request

Once the changes are pushed, you can proceed to create a pull request for the original repository using GitHub's interface. If you now go to `https://github.com/YOUR-USERNAME/start-oss` (Replace `YOUR-USERNAME` with your GitHub username.) You will see a notification by GitHub to create a pull request.

If you are in the workshop, feel free to give your mentor/ instructor a nudge so they can have a look at your pull request.

Congratulations! You have now started your OSS contribution journey. Happy contributing!
