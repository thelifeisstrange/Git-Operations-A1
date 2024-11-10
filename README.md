## Instructions

### 1. Create a Repository

1. Open a terminal and navigate to the directory where you want to create the repository.
2. Create a new directory and initialize it as a Git repository:

   ```bash
   mkdir git-assignment-repo
   cd git-assignment-repo
   git init
   ```

3. Create an initial commit to establish a base for the repository:
   
   ```bash
   echo "Initial commit" > README.md
   git add README.md
   git commit -m "Initial commit"
   ```

---

### 2. Create Branches

1. To create a new branch named `feature-branch`, run:

   ```bash
   git branch feature-branch
   ```

2. Switch to `feature-branch`:

   ```bash
   git checkout feature-branch
   ```

   - Alternatively, use `git checkout -b feature-branch` to create and switch to the branch in a single command.

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

4. **Push** your changes to the remote branch: Go to Github Create a repository without readme file, and follow the 1st instruction

create a remote : git remote add origin "your url"

   ```bash
   git push origin feature-branch
   ```

6. **Pull** the latest changes from the remote branch:

   ```bash
   git pull origin feature-branch
   ```

---

### 4. Merge and Rebase

1. **Merge** `feature-branch` into `master`:

   ```bash
   git checkout master
   git merge feature-branch
   ```

2. **Directly Rebase** `feature-branch` onto `master`:

   ```bash
   git checkout feature-branch
   git rebase master
   ```

> **Note**: This command directly re-applies the changes from `feature-branch` onto `master` without any interactive rebase. It rewrites the commit history to make it appear as if the changes in `feature-branch` were made on top of the latest `master`.

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

Force delete a **local branch** (if it hasn’t been merged):

   ```bash
   git branch -D feature-branch
   ```

---

### 7. Undo Commits

Undo the last commit and unstage changes:

   ```bash
   git reset HEAD~1
   ```

