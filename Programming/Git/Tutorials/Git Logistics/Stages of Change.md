---
---
---
# Stages of Change
File changes must cross several stages before appearing **remote**ly.
Whether added, modified in some way, or deleted, it must be _controlled_ for.
All changes are on the individual's system and will stay local.
Use the `Source Control` tab in VSCode to continue.


Each change labels the file according to what makes it different in the repository. 
- **(D) eleted** - Gone
- **(A) dded** - New
- **(R\) enamed** - Name
- **(T\) ypechange** - Reference
- **(S) ubmodule** - Child
- **(C\) onflict** - Error
- **(U) ntracked** - Absent
- **(M) odified** - Content
---
For a change to enter the repository, it must become **Staged**.
Click the `+` next to add the file to the list of changes to submit.
Without further intervention, that change will not enter the repository.

When comfortable with the changes present in these files, they must be **commit**ed.
At the top, enter a message that describes the exact changes and click the `Checkmark` above.
This will **commit** the changes to the repository and appear in the remote branch.

This branch, even if files drawn from the **main** branch were changed, will **not** affect other branches.

---