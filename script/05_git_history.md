# 5. Git History

Git is designed to keep a detailed history of everything you do in your repository. This history allows you to review and revert to previous states, making it an essential feature for tracking changes and collaborating with others. You can use commit hashes or tags to set the state of your repository to a specific commit, similar to switching branches.

## 5.1 Viewing the History of a Repository

To access the history of your Git repository, the `git log` command provides a comprehensive view of past commits. The simplest form of this command, `git log`, displays the commit hash, author, date, and message for each commit.

```sh
commit 990a517a04ab89f2ffd99d93b22ac99172772609
Author: Your Name <your-mail@example.com>
Date:   Sun Jul 11 12:36:11 2022 +0200

    my first commit
```

For a more concise and graphical representation of your commit history, you can use:

```sh
git log --all --graph --oneline
```

This command produces an output like the following:

```sh
* ae00104 add AUTHORS file
* 6a7ba4a add new line to README.md
* 990a517 my first commit
```

In this example, `--graph` creates a visual representation of the branch structure, while `--oneline` condenses each commit into a single line for easier readability.

The `git log` command offers numerous options to customize the output. Some useful options include:

- `--author=<author>`: Filter commits by a specific author.
- `--since=<date>`: Show commits more recent than a specific date.
- `--until=<date>`: Show commits older than a specific date.
- `--grep=<pattern>`: Search commit messages for a specified pattern.

## 5.2 Viewing the Diff of a Commit

To see what changes were introduced in a particular commit, you can use the `git diff` command along with the commit hash. This command shows the differences between the specified commit and its parent.

```sh
git diff <commit_hash>^ <commit_hash>
```

For example:

```sh
git diff 990a517^ 990a517
```

Alternatively, you can use `git show` to view the diff along with the commit details:

```sh
git show <commit_hash>
```

This command displays the commit metadata (author, date, message) and the diff of the changes introduced in that commit.

## 5.3 Viewing the History of a File

If you need to view the history of a specific file, you can use `git log` with the file path. This command lists all commits that modified the specified file.

```sh
git log -- <file_path>
```

For example:

```sh
git log -- README.md
```

To see the differences introduced to the file in each commit, you can use:

```sh
git log -p -- <file_path>
```

This command provides a patch (diff) for each commit that modified the file.

## 5.4 Undoing Changes

There are several ways to undo changes in Git, depending on the scenario:

### Undoing Local Changes

If you want to discard local changes in your working directory, you can use:

```sh
git checkout -- <file_path>
```

This command reverts the file to the last committed state.

### Undoing a Commit

To undo the last commit but keep the changes in your working directory, use:

```sh
git reset --soft HEAD~
```

If you want to discard the last commit and the changes, use:

```sh
git reset --hard HEAD~
```

### Reverting a Commit

If you need to undo a specific commit that has already been pushed, you can create a new commit that reverses the changes:

```sh
git revert <commit_hash>
```

This command creates a new commit that undoes the changes introduced by the specified commit.

## 5.5 Tagging Commits

Tags in Git are a way to mark specific points in the repository's history, usually used to indicate important releases. Unlike branches, tags are static and do not change once created.

To list all tags in your repository, use:

```sh
git tag --list
```

You can also filter tags using wildcards, such as:

```sh
git tag --list v2*
```

To create a tag at the current commit, use:

```sh
git tag <tag_name>
```

For example, to create a lightweight tag named `v1.0`, you would run:

```sh
git tag v1.0
```

If you want to add a message to the tag, which can include information about the tag, use:

```sh
git tag -a <tag_name> -m "your message"
```

For instance:

```sh
git tag -a v1.0 -m "Initial release"
```

To tag a specific commit, provide the commit hash:

```sh
git tag <tag_name> <commit_hash>
```

To view details about a tag, use:

```sh
git show <tag_name>
```

This command displays the commit details and any tag metadata, such as the tagger and message.

## 5.6 Navigating the Project History

Commit hashes and tags are valuable for navigating the project's history. You've already learned how to switch between branches. Similarly, you can check out any commit or tag to set your working directory to the state it was in at that point in time.

To check out a specific commit, use:

```sh
git checkout <commit_hash>
```

After checking out a commit, you can create a new branch from that state if needed:

```sh
git checkout -b <new_branch_name>
```

To check out a specific tag, use the same `checkout` command but with the tag name:

```sh
git checkout <tag_name>
```

This is especially useful for reviewing or reverting to specific versions of your project, such as when fixing bugs in a previous release or understanding changes made in a particular version.

By mastering these commands, you can effectively manage and navigate the history of your Git repository, making it easier to track changes, collaborate with others, and maintain a clean project history.