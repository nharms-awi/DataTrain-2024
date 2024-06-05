# Setup your environment

To ensure a smooth start to the course on Monday, June 03, 2024, you'll need to install certain software, create a GitHub account, and configure your setup.

If you already have a functioning Git environment and a GitHub account, feel free to skip ahead to [Verify your setup](#verify-your-setup). However, if you're missing any of these components, please follow the provided steps to establish your environment prior to the course commencement.

## Install git

Install the latest version of git (2.45.1 or newer) on your machine.
In addition to various security updates, some commands have been introduced or changed in the latest updates.
Downloads and instructions can be found at [git-scm.com/downloads](https://git-scm.com/downloads).
Please follow the instructions depending on your operating system.
After successful installation you should have "Git CMD", "Git Bash" and some other tools on your Windows machine.

Try opening a terminal, Git Bash on Windows or any terminal on Linux or Mac OS.
I will refer to this as `bash` from now on.

Type the following command into your Bash:

```bash
git --version
```

Depending on your system, you should get a response like this:
- `git version 2.45.1` or
- `git version 2.45.1.windows.1`

## Configure git

Before we work with git, we need to provide your name and email address.
This is required for commits that you create.

### Step 1 - Check the Git configuration for name and mail

First, check if you have set this in the past or if you already had git installed. Enter the following into your bash:

```bash
git config --get user.name
git config --get user.email
```

### Step 2 -- Set your name and mail
If the answer is blank, enter your name and email address.
To do this, type the following commands, replacing the name and email address with your data in your bash:

```bash
git config --global user.name "Firstname Surname"
git config --global user.email "mail@example.com" 
```

Then check the output again using the commands from [Step 1].(#step-1---check-git-configuration-for-name-and-mail)

You should get a response like this:
```bash
$ git config --get user.name
Firstname Surname

$ git config --get user.email
mail@example.com
```

## Setup SSH key

To use GitHub conveniently, you need an SSH key.
If you don't have a private and public SSH key yet, please create one.

### Step 1 - Check for an existing SSH key
Open your bash and enter this command

```bash
ls -al ~/.ssh
```

If you have used ssh and ssh keys before, it will look something like this:

```bash
$ ls -al ~/.ssh
total 44
drwxr-xr-x 1 nharms 1049089    0 Jun 27 16:02 ./
drwxr-xr-x 1 nharms 1049089    0 Jun 27 16:34 ../
-rw-r--r-- 1 nharms 1049089 1325 Apr 26 17:56 config
-r--r--r-- 1 nharms 1049089 3326 Jan 18  2019 id_rsa
-rw-r--r-- 1 nharms 1049089  750 Apr 21 15:38 id_rsa.pub
-rw-r--r-- 1 nharms 1049089 4077 Jun 27 14:55 known_hosts
```

If there are any files called:
- `id_rsa`/`id_rsa.pub`
- `id_dsa`/`id_dsa.pub`
- `id_ecdsa`/`id_ecdsa.pub`
- `id_ed25519`/`id_ed25519.pub`
- or two files, one with and one without the `.pub` extension.

Then you already have an ssh key and should proceed with [setting up your GitHub account](#step-2---setup-ssh-key)
If the directory contains only the `known_hosts` file and perhaps a `config` file, or you receive an
error that `~/.ssh` does not exist, proceed to [Step 2](#step-2---generate-an-ssh-key)

### Step 2 - Generate an SSH key

```bash
ssh-keygen -t ed25519 -C "mail@example.com"
```

1. choose a file name or use the default name by pressing the Enter key.
2. choose a password. This must be entered if you are using this ssh key. You can leave it blank if you do not want to set one up.
3. repeat the same password. Leave it blank if you did not set one up before.
4. get a random piece of art. You are done.

This is an example output:
```bash
$  ssh-keygen -t ed25519 -C mail@example.com
Generating public/private ed25519 key pair.
Enter file in which to save the key (~/.ssh/id_ed25519):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in id_ed25519_awi
Your public key has been saved in id_ed25519_awi.pub
The key fingerprint is:
SHA256:eQI862Q7Nk6HoUrImp+22uWxUrXDIXeXhPaYAeQwlFQ mail@example.com
The key's randomart image is:
+--[ED25519 256]--+
|   o=+E. .       |
|    .=  + .      |
|      =. * .     |
|    . +++.+      |
|     ==+S..      |
|..  .=++ o       |
|....+ O..        |
|.+o= * +         |
|++*oo .          |
+----[SHA256]-----+
```

## Set up GitHub account

For the second part of the course we will use GitHub.
You will need an account and some configurations to participate on your computer.

### Step 1 - Create account

If you don't have a GitHub account yet, go to the [github.com sign up Page](https://github.com/signup?ref_cta=Sign+up). Otherwise, proceed with [Step 2](#step-2---generate-an-ssh-key).

### Step 2 - Setup SSH key

The public part of your key can be known to everyone.
To enable access to your account, you need to add the public key to GitHub.

Copy the contents of your `.pub` file.

```bash
$ cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lHJK3FMAsmesoIAOk3xSVgqmS1bGhfBUn8rpIDgIYb8i8vNMfEU/2s1Ru mail@example.com
```

1. go to your [SSH and GPG keys](https://github.com/settings/ssh/new) settings in github.com.
2. write a title for this key and copy the answer from the previous command into the key field.
3. click _Add SSH key_.

For more detailed instructions, see the [GitHub documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Verify your setup

```bash
git clone git@github.com:nharms-awi/sign-test.git
cd sign-test
git switch -c $(git config --get user.email)
echo $(git config --get user.name) >> participants.md
git add participants.md
git commit -m "I, $(git config --get user.name), completed the setup"
git log
```

The last command should get you a response like:

```bash
commit 018ce0ba29fab3413f0e3207159ec9bf8e383d24 (HEAD -> nico.harms@awi.de)
Author: Nico Harms <nico.harms@awi.de>
Date:   Wed May 29 12:23:51 2024 +0200

    I, Nico Harms, completed the setup
```

If your output is not similar, there seems to be a problem with the setup.
Take a look at the error message you received.
If you can't fix this issue yourself, please send me a message (nico.harms@awi.de)

## Optional: Signing your commits

To digitally sign your commits, you can create a GPG key

Please follow the instructions on the [GitHub Documentation](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key) page.

After you have created your GPG key and added it to GitHub.
Add the following configuration to git. Replace `<key>` with your key from the `gpg --armor --export <key>` command.

```bash
$ gpg --list-secret-keys --keyid-format=long
/Users/hubot/.gnupg/secring.gpg
------------------------------------
sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
uid                          Hubot <hubot@example.com>
ssb   4096R/4BB6D45482678BE3 2016-03-10
```

Replace `3AA5C34371567BD2` with with yours in the following command.

```bash
git config --global user.signingkey 3AA5C34371567BD2
```

You may try the following commands, but this time add the `-S` option to your commit command, which is shorthand for `--gpg-sign`.

```bash
echo $(git config --get user.name) >> participants.md
git add participants.md
git commit -m "I, $(git config --get user.name), just signed my commit"
git log --show-signature
```

```bash
commit 018ce0ba29fab3413f0e3207159ec9bf8e383d24 (HEAD -> nico.harms@awi.de)
gpg: Signature made Wed May 29 12:23:51 2024 CEST
gpg:                using RSA key A462CD04E3B5F8753E782A6F3D9457FAB4414D33
gpg: Good signature from "Nico Harms <nico.harms@awi.de>" [ultimate]
Author: Nico Harms <nico.harms@awi.de>
Date:   Wed May 29 12:33:51 2024 +0200

    I, Nico Harms, just signed my commit
```
