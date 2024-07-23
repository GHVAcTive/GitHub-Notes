# Git Commands Cheat Sheet 🚀

## Moving and Renaming Files 📂

```bash
git mv move.txt MOVE.txt
```
- Moves and renames `move.txt` to `MOVE.txt`.

## Cloning a Repository 🐙

```bash
git clone <http>
```
- Clones the repository from the provided HTTP link.

## Committing Changes 💾

```bash
git commit -m "Comment"
```
- Commits changes with a message.

## Setting Global Username and Email 📧

```bash
git config --global user.name "Your Username"
git config --global user.email "your.email@example.com"
```
- Sets the global username and email for Git.

## Switching Branches 🌿

```bash
git checkout <branch-name>
```
- Switches to the specified branch.

## Pushing to Remote Repository ⬆️

```bash
git push origin main
```
- Pushes the local changes to the remote `main` branch.

## Pulling from Remote Repository ⬇️

```bash
git pull origin main
```
- Pulls the latest changes from the remote `main` branch.

## Checking Remote URLs 🌐

```bash
git remote -v
```
- Displays the URLs of remote repositories.

## Listing Branches 🌲

```bash
git branch
```
- Lists all local branches.

## Checking Status 🕵️

```bash
git status
```
- Displays the state of the working directory and staging area.

## Viewing Commit Log 📜

```bash
git log
```
- Shows the commit history.

## Creating and Switching to a New Branch 🌳

```bash
git checkout -b <branch-name>
```
- Creates a new branch and switches to it.

## Deleting a File ❌

```bash
del file.txt
```
- Deletes `file.txt` from the working directory.

## Merging Branches 🔀

```bash
git merge <branch>
```
- Merges the specified branch into the current branch.

## Initializing a Repository 🆕

```bash
git init
```
- Initializes a new Git repository.

## Staging Changes 📤

```bash
git add .
```
- Stages all changes in the working directory.

## Echoing Null to a File 🔇

```bash
echo $null >> file name
```
- Appends `null` to the specified file.

## Creating a New File 📄

```bash
touch filename.txt
```
- Creates a new empty file named `filename.txt`.

## Appending to a File 📝

```bash
cat >> filename
```
- Appends content to the specified file until `EOF` is reached.


## Access of Remote Control 📝

```bash
git remote add origin <link>

```
- Give the Remote access to the original GitHub File When we created in Local Repo.

# Git Branch Management 📂

## Renaming a Branch ✏️

To rename a branch, follow these steps:

1. **Switch to the branch you want to rename**:
    ```bash
    git checkout old-branch-name
    ```

2. **Rename the branch**:
    ```bash
    git branch -m new-branch-name
    ```
   - Alternatively, you can rename a branch without switching to it:
     ```bash
     git branch -m old-branch-name new-branch-name
     ```

3. **Push the renamed branch to the remote repository**:
    ```bash
    git push origin new-branch-name
    ```

4. **Delete the old branch from the remote repository**:
    ```bash
    git push origin --delete old-branch-name
    ```

5. **Update the upstream branch (if needed)**:
    ```bash
    git push --set-upstream origin new-branch-name
    ```

## Deleting a Branch 🗑️

To delete a branch, follow these steps:

### Locally

1. **Delete the branch locally**:
    ```bash
    git branch -d branch-name
    ```
    - If the branch hasn't been merged, use:
      ```bash
      git branch -D branch-name
      ```

### Remotely

1. **Delete the branch from the remote repository**:
    ```bash
    git push origin --delete branch-name
    ```

### Example Scenario 🌟

Let's say you have a branch called `feature/login` that you want to rename to `feature/auth` and then delete it after merging. Here's how you can do it:

1. **Rename the branch**:
    ```bash
    git checkout feature/login
    git branch -m feature/auth
    git push origin feature/auth
    git push origin --delete feature/login
    git push --set-upstream origin feature/auth
    ```

2. **Merge and delete the branch**:
    ```bash
    git checkout main
    git merge feature/auth
    git branch -d feature/auth
    git push origin --delete feature/auth
    ```


# Vim Command: `:q!` 🚪❌

## What is `:q!`? 🤔

`:q!` is used in Vim to **quit without saving changes**. This is useful if you want to discard modifications.

## How to Use `:q!`? 🛠️

1. **Open Vim**:
   ```sh
   vim filename.txt
   ```

2. **Make Changes** ✍️:
   - Edit the file as needed.

3. **Quit Without Saving**:
   - Press `Esc` to enter Normal mode.
   - Type `:q!` and press `Enter`.
     ```vim
     :q!
     ```

## Example 📖

```sh
vim example.txt
```
```vim
:q!
```

## Related Commands 🔍

- `:q` - Quit (prompts to save if there are unsaved changes).
- `:wq` - Save and quit.
- `:w` - Save without quitting.
