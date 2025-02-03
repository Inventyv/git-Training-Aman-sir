# git-training

This repository is designed to teach you Git and GitHub in detail. It covers everything from basic Git configuration to creating repositories, managing branches, setting branch rules, and making pull requests.

## Table of Contents

- [Basics of Git](#basics-of-git)
- [Configuring Git](#configuring-git)
- [Creating a Repository](#creating-a-repository)
- [Creating and Managing Branches](#creating-and-managing-branches)
- [Setting Branch Rules](#setting-branch-rules)
- [Visualizing Branches](#visualizing-branches)
- [Pull Requests](#pull-requests)

---

## Basics of Git

Git is a powerful version control system that helps you track changes in your codebase over time. It allows multiple people to collaborate on the same project, ensuring that all changes are tracked and managed efficiently.

### Configuring Git

Before using Git, you need to configure it with your username and email so that your commits are properly attributed to you. Run the following commands to set your global username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

### Result:

After running these commands, Git will use this information for all your commits, ensuring proper attribution.

## Creating a Repository

### Initializing a Git Repository

To create a new Git repository and push your files to GitHub, follow these steps:

1. **Create a new repository on GitHub**:

   - Navigate to your GitHub account and click on the "New repository" button.
   - Name the repository (e.g., `git-training`).
   - Choose whether you want the repository to be public or private.
   - Click "Create repository".

   **Result:** You will see an empty repository created with instructions to add files.

2. **Clone the repository to your local machine**:

   - Copy the repository URL provided by GitHub.
   - In your terminal, run the following command to clone the repository to your local machine:

   ```bash
   git clone <repository_url>
   ```

   **Result:** This creates a local copy of the repository on your machine.

3. **Create a file (e.g., `index.html`)** in your repository. You can create this file manually or with the following command:

   ```bash
   touch index.html
   ```

   **Result:** A new file named `index.html` is created in your repository folder.

Here is a practical illustration:
![](https://imgur.com/cTErh36.png)

**Explanation:** The image shows the repository setup in the local machine, and an `index.html` file added.

### Committing and Pushing Changes

1. Add the new file to Git tracking:

   ```bash
   git add index.html
   ```

   **Result:** The file is staged for commit.

2. Commit the file with a message:

   ```bash
   git commit -m "Added index.html"
   ```

   **Result:** The changes are now committed locally with a message.

3. Push the file to GitHub:

   ```bash
   git push origin main
   ```

   **Result:** The `index.html` file is now visible on GitHub.

This is how it looks on GitHub after adding the file:
![](https://imgur.com/9EUqDQP.png)

## Creating and Managing Branches

To create multiple branches for different features:

```bash
git branch dev
git branch alpha
git branch beta
```

**Result:** Three new branches `dev`, `alpha`, and `beta` are created.

To switch between branches:

```bash
git checkout dev
```

**Result:** You are now working in the `dev` branch.

To push all branches to GitHub:

```bash
git push -u origin dev
```

```bash
git push -u origin alpha
```

```bash
git push -u origin beta
```

**Result:** All branches are now available on GitHub.

Here is an image showing the branches created:
![](https://imgur.com/5DPjz0Z.png)

## Setting Branch Rules

To enforce branch protection rules on GitHub:

1. Navigate to your repository on GitHub.
2. Go to **Settings** > **Branches**.
3. Under **Branch protection rules**, click **Add rule**.
4. Enter the branch name you want to protect (e.g., `main`).
5. Select rules such as:
   - Require pull request reviews before merging.
   - Require status checks to pass before merging.
   - Restrict who can push to the branch.
6. Click **Save changes**.

**Result:** The selected branch will now have enforced rules, preventing direct commits and ensuring a controlled workflow.

## Pull Requests

To create a pull request:

1. Go to GitHub and navigate to your repository.
2. Click on the **Pull Requests** tab and then click **New Pull Request**.
3. In the pull request creation page:
   - Select the **base** branch (e.g., `main`).
   - Select the **compare** branch (e.g., `dev`).
   - GitHub will show the differences between these branches.
4. Click **Create Pull Request**.
5. Add a title and description explaining the changes.
6. Assign reviewers, labels, or projects if needed.
7. Click **Submit Pull Request**.
8. Once the pull request is reviewed, click **Merge Pull Request**.
9. Confirm the merge and delete the branch if it's no longer needed.

Here are images illustrating the process:

We are adding the protection rule for the branch here:
![](https://imgur.com/Ni0WyBq.png)

These are the available options to add rules from:
![](https://imgur.com/vdS33Rt.png)

Finalizing the pull request process:
![](https://imgur.com/dFZ9wgJ.png)

You can see the rule you added for the main branch here:
![](https://imgur.com/rAhixKs.png)

**Result:** The pull request is successfully merged into the main branch, ensuring a controlled and reviewed workflow.
