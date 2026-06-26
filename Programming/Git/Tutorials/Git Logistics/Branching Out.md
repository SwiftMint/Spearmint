---
---
---
# Branching Out

To switch between branches, use the keyword `checkout` or `switch` in Git.
 This can be helpful to check on original files or updated changes.

 To combine a branch with **main**, they must be **merge**d.
 Easily enough, this can be done with a **Merge Request** (**MR** for short).
 Git**Hub** (_not_ Git**Lab**) calls these **Pull Request**s (**PR**s for short).
In a given repository, drawing changes  from it is a **pull** while sending is a **push**.

While in **main**, click `...`, hover over `Branch`, and click `Merge Branch`.
Alternatively, type `Merge` for GitLab's VSC command.
It will ask for a branch to merge *from*. Select the branch with the intended changes.

Then, click `Publish Branch` to add it to a Public or Private repository.

If changes were published to the **remote** repository, they will not appear in the local files.
To "catch up" to a current branch, click `Synchronize Changes`.
This will bring up a popup, stating:

This action will **pull** and **push** commits from and to `branch/repository-name`.
Click OK.

---