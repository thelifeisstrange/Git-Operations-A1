## Instructions

### 1. Create a Repository

1. Open a terminal and navigate to the directory where you want to create the repository.
2. Create a new directory and initialize it as a Git repository:

   ```bash
   mkdir git-assignment-repo
   cd git-assignment-repo
   git init
   ```

### 2. Create Branches

1. To create a new branch named `feature-branch`, run:

   ```bash
   git branch feature-branch
   ```

2. Switch to `feature-branch`:

   ```bash
   git checkout feature-branch
   ```

---

### 3. Add, Commit, Push, and Pull

1. **Add** files to staging. For example, create a file called `sample.txt`, then stage it:

   ```bash
   echo "Hello, World!" > sample.txt
   git add sample.txt
   ```

2. **Commit** your changes:

   ```bash
   git commit -m "Add sample.txt with initial content"
   ```

3. Make another change for demonstration. Edit `sample.txt`, then:

   ```bash
   echo "This is a new line." >> sample.txt
   git add sample.txt
   git commit -m "Update sample.txt with new content"
   ```

4. **Push** your changes to the remote branch:

   ```bash
   git push origin feature-branch
   ```

5. **Pull** the latest changes from the remote branch:

   ```bash
   git pull origin feature-branch
   ```

---

### 4. Merge and Rebase

1. **Merge** `feature-branch` into `main`:

   ```bash
   git checkout main
   git merge feature-branch
   ```

2. **Rebase** `feature-branch` onto `main`:

   ```bash
   git checkout feature-branch
   git rebase main
   ```

> **Note**: Be careful with rebasing when working with shared branches, as it rewrites commit history.

---

### 5. Squash Commits

1. Squash the last two commits on `feature-branch` into a single commit:

   ```bash
   git rebase -i HEAD~2
   ```

2. In the interactive rebase screen, change `pick` to `squash` for the second commit.
3. Save and close the editor, then update the commit message if desired.

---

### 6. Delete Branches

delete a **local branch** (if it hasn’t been merged):

   ```bash
   git branch -D feature-branch
   ```


### 7. Undo Commits


Undo the last commit and unstage changes:

   ```bash
   git reset HEAD~1
   ```
