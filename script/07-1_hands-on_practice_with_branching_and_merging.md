# 7. Hands-On Practice with Branching and Merging

## Task 1: Setting Up the Initial Repository

**Initialize a Git Repository**: Create a new directory for your project and initialize a Git repository.

```bash
mkdir merge_conflict_demo
cd merge_conflict_demo
git init
```

**Create a Sample File and Make Initial Commit**: Create a file named `example.txt` with some initial content and commit it.
   
```bash
echo "This is the first line of the file." > example.txt
git add example.txt
git commit -m "Initial commit with example.txt"
```

> **Note**: The `echo` command is used to write text to a file. The `>` operator is used to redirect the output of the `echo` command to a file.

## Task 2: Create and Work on Branches

**Create a New Branch and Make Changes**: Create a new branch named `branch1` and modify `example.txt`.

```bash
git switch --create branch1
echo "This is a line added in branch1." >> example.txt
git add example.txt
git commit -m "Add a line in branch1"
```

> **Note**: The `>>` operator is used to append text to a file.

**Switch Back to Main Branch and Make Conflicting Changes**: Switch back to the `main` branch and make changes to the same file.

```bash
git switch main
echo "This is a line added in main." >> example.txt
git add example.txt
git commit -m "Add a line in main"
```

## Task 3: Force a Merge Conflict

**Merge `branch1` into `main`**: Attempt to merge `branch1` into `main`, which will result in a merge conflict.

```bash
git merge branch1
```

## Task 4: Resolve the Merge Conflict

**Identify and Resolve the Conflict**: Git will notify you of the conflict. Open `example.txt` to see the conflict markers and resolve the conflict.

Conflict Markers in `example.txt`:
  
```txt
<<<<<< HEAD
This is a line added in main.
======
This is a line added in branch1.
>>>>>> branch1
```

**Resolve the Conflict**: Choose how to resolve the conflict (keep one change, merge them, or create a new line). For this example, let's merge them:

```txt
This is the first line of the file.
This is a line added in main.
This is a line added in branch1.
```

**Stage the Resolved File and Commit the Merge**: After resolving the conflict, stage the file and commit the merge.

```bash
git add example.txt
git commit -m "Resolved merge conflict between main and branch1"
```

### Task 5: Verify the Merge

**Check the Commit History**: Verify the merge by looking at the commit history.

```bash
git log --oneline --graph
```

## Go Wild!

Feel free to experiment with creating more branches, making changes, and merging them to practice resolving merge conflicts. This hands-on practice will help you become more comfortable with Git's branching and merging capabilities.