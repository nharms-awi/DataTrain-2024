# Hands-On: Practice with Basic CLI Commands

# CLI Training Assignment

Welcome to your CLI training assignment! This guided exercise will help you practice and master basic CLI commands. Follow the steps below to complete the tasks.

## Guided Exercises to Practice Basic CLI Commands

### Step 1: Create a folder in your home directory called `repositories`
Command:
  ```bash
  mkdir ~/repositories
  ```

> Note: The `~` symbol represents your home directory. On a german keyboard, you can find the `~` symbol by pressing `Alt Gr` + `^`, then `Space`. On a US keyboard, you can find the `~` symbol by pressing `Shift` + `` ` ``.

Move into the repositories directory:

```bash
cd ~/repositories
```

### Step 2: Create a folder in your home directory called `datatrain-cli`
Command:
  ```bash
  mkdir datatrain-cli
  ```

### Step 3: Navigate to the `datatrain-cli` folder
Command:
  ```bash
  cd datatrain-cli
  ```

### Step 4: Create a file called `hello.txt`
Command:
  ```bash
  touch hello.txt
  ```

### Step 5: Write `Hello, World!` in the `hello.txt` file

Depending on your preference, you can use `nano` or `vim` to edit the file.

- Using `nano`:
  ```bash
  nano hello.txt
  ```
  - Type `Hello, World!`
  - Save and exit by pressing `Ctrl + X`, then `Y`, then `Enter`

- Using `vim`:
  ```bash
  vim hello.txt
  ```
  - Press `i` to enter insert mode
  - Type `Hello, World!`
  - Press `Esc`, then type `:wq` and hit `Enter` to save and exit

### Step 6: View the contents of the `hello.txt` file
Command:
  ```bash
  cat hello.txt
  ```

### Step 7: Update the contents of the `hello.txt` file to `Hello, DataTrain!`
- Using `nano`:
  ```bash
  nano hello.txt
  ```
  - Replace `Hello, World!` with `Hello, DataTrain!`
  - Save and exit by pressing `Ctrl + X`, then `Y`, then `Enter`

- Using `vim`:
  ```bash
  vim hello.txt
  ```
  - Press `i` to enter insert mode
  - Replace `Hello, World!` with `Hello, DataTrain!`
  - Press `Esc`, then type `:wq` and hit `Enter` to save and exit

### Step 8: Create a new folder called `subfolder`
Command:
  ```bash
  mkdir subfolder
  ```

### Step 9: Copy the `hello.txt` file to the `subfolder`
Command:
  ```bash
  cp hello.txt subfolder/
  ```

### Step 10: Output the contents of the `subfolder/hello.txt` file
Command:
  ```bash
  cat subfolder/hello.txt
  ```

### Step 11: Modify the contents of `hello.txt` in the `datatrain-cli` folder
- Using `nano` or `vim`, open `hello.txt` and make changes of your choice. For example, you can add another line of text.

### Step 12: Delete the `subfolder` and its contents
Command:
  ```bash
  rm -r subfolder
  ```

### Step 13: Rename the `hello.txt` file to `README.md`
Command:
  ```bash
  mv hello.txt README.md
  ```

### Step 14: List the contents of the directory
Command:
  ```bash
  ls
  ```

### Step 15: Go wild!
In your `datatrain-cli` directory, practice using these commands:
- Create multiple files using `touch`.
- Edit files using `nano` or `vim`.
- Move files around using `mv`.
- Copy files using `cp`.
- Delete files and directories using `rm`.
- List files and directories using `ls`.
- Navigate between directories using `cd`.

Explore and have fun with these commands to become more comfortable with the CLI.