# Merging and Rebasing
The **base** from _Resolving Changes_ is resolved at `M [#4]`.

Another feature will be created in a new branch.
Let's call this branch `Exciting!`.

This feature is going to take quite a while.
Once completed, an MR could be full of conlicts.

It is a good practice to occasionally merge **main** into `Exciting!`.
This ensures that the most up-to-date code is in `Exciting!`.
Perhaps the updates help `Exciting!`'s progress or even solve prior bugs.

Once merged back onto **main**, the **commit**s and conflicts appear.
Each conflict, merge, commit, etc. is all visible.

After time, this can become quite unsavory to look at.
Additionally, many are not contributing helpful information.

An example is each time **main** is merged into `Exciting!`.
Let's say this is done six times over the course of development.

Now, six commits are essentially useless to display in history.
**Version control** preserves these commits as intended.

To simplify analysis of the version history, there are three options.
A **squash**, **rebase**, or both.

**Rebasing** is exactly as it sounds.
`Exciting!` began with a **base** of `M [#4]`.
After the long period of development, **main** is at `M [#25] `.

After a **rebase**, a specific branch becomes the **base** of the target branch.
When merged fully into **main**, all useless merges are removed.

Keep in mind that a **rebase** rewrites its internal history to match **main**.
In doing so, it applies the commits one-by-one.
This is in line with the intent of a **rebase**.

**Merge**s will show each and every historic commit.
**Rebase**s will show the _intended_ commits (only differences from **main**).

If multiple commits are pushed to a **remote**, do not **rebase**.
A rebase will change the hash with its history and lead to a Git mismatch.

Solving conflicts in a rebase may lead to a cascade of conflicts to solve.
A **rebase** pauses during each conflict as it applies commits one-by-one.

These require a .git **add** instead of **commit** to **continue**.
Once **continue**d and no conflicts persist, a **rebase** is completed.

Then, a **merge** can happen if target (**main**) is identical to current (`Exciting!`).
This is a **fast-forward** merge, what a typical **merge** refers to.

Without a **rebase**, a merge can still occur. It is then called a **merge commit**.
This commit includes the history of _both_ branches, leaving excess commits.

---