# 2 What is git?

> Git is a free and open source distributed version 
> control system designed to handle everything from 
> small to very large projects with speed and efficiency.
> 
> [git-scm.com](https://git-scm.com/)

Git, created by Linus Torvalds in 2005, is now the most widely used version control system. Initially developed to manage the Linux kernel’s source code, Git quickly gained popularity due to the kernel’s high status in the developer community and Git’s powerful capabilities.


## 2.1 How Git Works

### Distributed Version Control

Unlike traditional version control systems that rely on a central server to store all versions of a project, Git uses a distributed approach. Each developer has a local copy of the entire repository, including its complete history. This decentralization offers several advantages:

- Speed: Local operations are extremely fast because they do not require network access.
- Flexibility: Developers can work offline and commit changes locally.
- Resilience: The project’s history is replicated across multiple locations, reducing the risk of data loss.

### Snapshots, Not Differences

Many version control systems store information as a list of file-based changes. Git, however, stores data as snapshots of the entire repository. Each time you commit a change, Git records a snapshot of all your files, and if files have not changed, Git doesn’t store the file again, but a link to the previous identical file.

### Branching and Merging

One of Git’s most powerful features is its branching model. A branch in Git is a lightweight movable pointer to one of these snapshots. By default, Git creates a branch named `main`, but you can create new branches to develop features, fix bugs, or experiment, all without affecting the main branch. Once your work is ready, you can merge your changes back into the main branch. This enables:

- Parallel Development: Different features can be developed simultaneously.
- Isolation: New work can be done without disturbing the main codebase.
- Traceability: The history of changes is easy to follow.

### Integrity

Git has a built-in mechanism to ensure data integrity. Everything in Git is checksummed before it is stored, and every object is identified by a SHA-1 hash. This means that it is impossible to change the contents of any file or directory without Git knowing about it.

## 2.2 The Areas of Git

Git organizes your work into several areas, each serving a specific purpose in the workflow. Understanding these areas is crucial for effective version control.

### Working Directory

The working directory is where you perform your day-to-day work. It contains the files you are currently editing. When you clone a repository, Git copies all the files from the repository and places them in the working directory. Any changes you make to the files are made in the working directory.

### Staging Area

The staging area, also known as the index, is a place where you can format and review your changes before committing them. When you add changes to the staging area using git add, Git records your intent to include those changes in the next commit. The staging area allows you to control what will be included in the commit, making it easier to manage large sets of changes.

### Local Repository

The local repository is where Git stores the history of all your commits. It contains all the snapshots of your project. When you commit changes, Git moves them from the staging area to the local repository, creating a new snapshot of the project’s state. The local repository allows you to work on your project independently of others.

### Remote Repository

The remote repository is a version of your project that is hosted on the internet or another network. It is used to share your work with others and collaborate on projects. The remote repository allows multiple developers to push their local commits and pull updates made by others. Popular services like GitHub, GitLab, and Bitbucket provide hosting for remote repositories, adding collaboration tools and features on top of Git.

### Workflow Summary

- Working Directory: Where you make changes to your files.
- Staging Area: Where you prepare changes for the next commit.
- Local Repository: Where your commits and project history are stored.
- Remote Repository: Where you share your project with others and collaborate.

## 2.3 Understanding Git as a Command Line Tool

Git is a command line tool with a large number of commands for controlling changes to your files. If you call the help information via `git --help` after installation, you will get an overview of the available commands.

```
$ git --help
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--config-env=<name>=<envvar>] <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.
```

Each command comes with its own help section, accessible by appending `--help` to the command (e.g., `git init --help`). This provides a detailed description and available options for that command.

It’s important to distinguish Git from platforms like GitHub or GitLab. Git is the underlying version control tool, while GitHub, GitLab, and similar services offer hosting and collaboration features that leverage Git’s capabilities.
