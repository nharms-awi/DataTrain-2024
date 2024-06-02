# 4. Hands-On: Practice with Basic Git Commands

Now that you understand the basic Git commands, let's practice by creating and working with your first repository.

## 4.1 Step-by-Step Instructions

### Step 1: Initialize a Repository

1. Open your terminal or command prompt.
2. Navigate to the directory where you want to create your project.
3. Initialize a Git repository:

    ```bash
    git init -b main
    ```

### Step 2: Create and Add a File

1. Create a new file named `README.md`:

    ```bash
    echo "# My First Git Project" > README.md
    ```

2. Check the status of your repository to see the untracked file:

    ```bash
    git status
    ```

    You should see something like:

    ```bash
    On branch main

    No commits yet

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
            README.md

    nothing added to commit but untracked files present (use "git add" to track)
    ```

3. Add the file to the staging area:

    ```bash
    git add README.md
    ```

4. Check the status again to see the staged changes:

    ```bash
    git status
    ```

    Now you should see:

    ```bash
    On branch main

    No commits yet

    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
            new file:   README.md
    ```

### Step 3: Commit Your Changes

1. Commit the changes with a message:

    ```bash
    git commit -m "Add README file"
    ```

2. Check the status one more time to ensure everything is committed:

    ```bash
    git status
    ```

    You should see:

    ```bash
    On branch main
    nothing to commit, working tree clean
    ```

### Step 4: Make Additional Changes

1. Edit the `README.md` file to add more content. For example, open it in a text editor and add:

    ```markdown
    ## Introduction

    This is my first project using Git.
    ```

2. Save the changes and check the status:

    ```bash
    git status
    ```

    You will see:

    ```bash
    On branch main
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   README.md
    ```

3. Add and commit the changes:

    ```bash
    git add README.md
    git commit -m "Update README with introduction"
    ```

### Step 5: View Commit History

1. To see the history of commits, use:

    ```bash
    git log
    ```

    This will show a list of commits with their messages and identifiers.


### Step 6: Go Wild!

Try to create more files, make changes, and commit them. Experiment with different Git commands to get a feel for how version control works. You could:

- Create new files using `touch`.
- Edit files using a text editor.
- Add and commit changes to see how Git tracks the history of your project.
- Use `git log` to explore the commit history.

## Conclusion

By following these steps, you've successfully created your first Git repository, added and committed changes, and viewed the commit history. This hands-on practice helps solidify your understanding of basic Git commands and their usage.