---
---
---
# How to Properly Control

Fitting the definition of the word, these files begin in a **Repository**, or "**repo**" for short.
These files in the repository need to be protected, as discussed in _Version Control & You_.

To do this, we need to create a different arm of the files, named a **Branch**.
By default, all files begin in a branch titled **main** or **master**.
Following that logic, never begin to edit any files on the **main** or **master** branch.

To create a new branch in Visual Studio Code (VSC or VSCode for short), use the Git extension.
Open commands with `Ctrl` + `Shift` + `P` and type in: `Git: Create Branch`.
Alternatively, click on the search bar and preface the same query with `>`.

Once selected, VSC will prompt the user to input a name for the branch.
When applicable, follow the provided Horizon Suite template.

**type/issue-number-brief-description**.
Spaces are automatically filled with a `-`:

There are **four** types at the time of writing:
- **Bug**
- Enhancements
  - **Feature**
  - **Improvement**
  - **Localization**

The **localization** type should be used for anything relating to **non-enUS** clients.
This especially applies when the purpose is to fix a bug that is not present in the enUS client. 

If the status bar is enabled, the new branch should appear on the left of the bar.

Without the right permissions, an individual cannot simply create a new branch for contributions.
This is ideal as all branches still reside in a project's repository.
Anyone with access to the project can view these branches.

Individuals who wish to contribute without proper permissions must copy the repository entirely.
This copy shows in that individual's account as their own project.
This is known as a **fork**. Alternatively, a repository can be **clone**d.

If a branch, clone, or fork lags behind the original repository, there are shortcuts to "catch up".

GitLab/GitHub's host of the repository is **Remote**. The actual files live on an individual's system.
When submitting changes, it then updates that remote repository.

Git's primary intent is to _control_ for changes.
Contributions cannot immediately pass into the **main** branch, or **main** for short.

---