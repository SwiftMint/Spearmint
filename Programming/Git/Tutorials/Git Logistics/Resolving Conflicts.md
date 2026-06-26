# Resolving Conflicts
In a collaborative setting, it is rare to never "cross paths" so-to-speak.
Conflicts can arise when multiple users attempt to edit the same file.

For the sake of example, let's call **main**, `M`.
Additionally, that a file was added with **commit** `[#1]`.

The **version control** would then show two different instances.

`M` --> `M [#1]`

At this point, let's decide to work on a feature for the project.
A branch is created to perform this without corrupting **main**.
Let's call this new branch, `New!`.

`New!` is made at `M [#1]`, making it identical to `M [#1]`.
The file present in `M [#1]` that is not in `M` would be in `New!`.

Once work is complete in `New!`, an MR can be performed into `M`.

However, in the time it took to complete `New!`, `M [#1]` has more commits.
`M [#2]` edited a file that `New!` edited.
`M [#3]` created a file. `M [#3A]` edited that same file.

The **version control** at that point would show the following instances.

`M` --> `M [#1]` --> `M [#2]` --> `M [#3]` --> `M [#3A]`

An **MR** performed onto **main** from `New!` would have conflicts.

`New!` doesn't have the edit **commit**ted in `M [#2]`.
`New!` also does not have the file **commit**ted `M [#3]`.
`New!` also does not that file's later edit in **commit** `M [#3A]`.

The **Version Control** seeks to integrate branches systematically.
Each **commit** comes with a time, date, and reason, among other things.

The reference point for this merge becomes `M [#1]`, the **base** of `New!`.
The primary conflict at this point is `M [#2]` with the changes in `New!`.

With some of the same lines edited, **version control** seeks to rectify this.

The current instance of **main** is `M [#3A]`, which becomes the **head** commit.
In comparison, the same lines edited in `New!` become the title of the **MR**.
We'll call the **MR**, `New!/Feature`.

Within VSC, the **head** commit is known as **Incoming**.
The changes in `New!/Feature` are known as **Current**.
The **base** display in its entirety can be toggled on/off.

The three options are to **accept**, **combine**, or **ignore** changes.
A **combination** will attempt to place both edits within the final file.
The **Preview** window displays the final output, which can be directly edited.

---


