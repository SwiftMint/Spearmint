# Git Command Terminal

### This begins with the assumption that **Git** is installed. <br> Documentation can be found online at https://git-scm.com/learn and https://git-scm.com/docs.
---
All subsequent `code blocks` are based on the Author's Terminal at time of writing.
All subsequent mentions of `I`, `Me`, `My`, `Mine`, or `other personal pronoun` refers to the Author.

---
#### **Git**, like any source language, has a multitude of commands available. Typically, these begin with `git`.

As described by the **Git Manual**:
> Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.

Using the **GitBash** terminal, I begin with the following already present in the terminal.
![GitBash Terminal stating the following: In Green: Antho@Avalar, In Magenta: MINGW64, In Yellow: ~/Desktop/Civil/Games/World of Warcraft/Horizon Suite/Working/Tutorials/Git Explained](Terminal_Directory.png)
- In Green: `Antho@Avalar`
    - `Antho` is the name of my `User` folder within `C:\Users`
    - `Avalar` is the name of my `System`
- In Magenta:
    - I use the `W`indows x`64` version of GitBash
- In Yellow:
    - Authored File's Directory:
      - On my `Desktop`
      - In the `Civil` Section
      - In `Games` Subsection
      - In `World of Warcraft` Subsection
      - In `Horizon Suite`'s Subsection
      - In `Working` Subsection
      - In `Tutorials` Subsection
      - In `Git Explained` Subsection
<br>

That same string results if `Enter` is pressed without a command.
If a command _is_ provided, `Enter` will submit that command. 
If an output is truncated, `Enter` will continue returning that command.
To exit a lengthy command return, press `q`.
To exit a terminal that becomes stuck in a command, press `Ctrl` + `C`.

**GitBash** typically requires a single dash (`-`) for an individual character command or a double dash (`--`) for a multiple character command.
Keep in mind the case of each command character. Any uppercase command will not function the same as any lowercase counterpart.

The terminal output for each command is very close to the information within their respective manual page.
However, the manual page offers slightly more information so I will be quoting the manual.
Note: Subcommand listings will not include their parent command's source.

All references will be made to the terminal output regardless of any source difference.
All terminal output is accurate as of time of writing.

Each command description will include that command and its execution, exactly as entered into the terminal.
Keep in mind that **GitBash** will match the _first_ available command. I will use this shortcut potential when possible.

See: `git.md`
---