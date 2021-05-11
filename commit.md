This is a template for structuring articles:

# Using `git commit`

[What are commits?](##Git~Commit)

[Use Cases](##Use~cases.)

[Commands](##Commands)

[Additional points](##Additional~points)

[Basic Workflow](##Basic~workflow)

<!-- Please change the above in case any heading are changed to be consistent with the file itself. Do replace '{component name} with the name of what's being worked on-->

## Git Commit

Record changes to the repository.

## Use cases.

- When you are done with your task.
- In a good state with working functionality.


## Commands

| Commands  | Description |
| --------  | ----------- |
|` command `| Information about what happens when using this particular command |
|` -m "commit msg", --message=<msg>`| Add a commit title to this commit (max 50 characters) |
| `-a` `--all` | Stages files that were modified or deleted. New files that you have not told Git about are unaffected |.
| `-p` `--patch` | The interactive patch selection interface choses which changes to commit within a file. Used with `git add --patch` to select separate "hunks" to decide which to commit  |
| `-C <commit>` `--reuse-message=<commit>`  | Take an existing commit object, and reuse log/authorship information when creating the commit |
| `-c <commit>` `--reedit-message=<commit> `  | Editor will be invoked so user can edit the commit message. |
| `--fixup=<commit>`  | ----------- |
| `--squash=<commit>`  | ----------- |
| `--reset-author`  | ----------- |
| `--short`  | When performing a `--dry-run`, gives the information in a shorthand format, implies the use of `--dry-run`. |
| `--branch`  | Show the branch and tracking information (even in short form) |
| `--porcelain`  | When doing a dry-run, give output in a porcelain-ready format. Which gives output an easy-to-parse format for scripts. Similar to short output, but will remain stable across Git versions regardless of user configuration. Implies `--dry-run` |
| `--long`  | When doing a `--dry-run`, give the output in the long-format. Implies `--dry-run` |
| `-z` `--null`  | ----------- |
| `-F <file>` `--file=<file>`  | Take the commit message from the given file. Use - to read the message from the standard input. |
| `--author=<author>`  | ----------- |
| `--date=<date>`  | Override the author date used in the commit. |
| `-t <file>` `--template=<file>`  | ----------- |
| `-s` `--signoff` `--no-signoff`  | ----------- |
| `-n` `--no-verify`  | ----------- |
| `--allow-empty`  | ----------- |
| `--allow-empty-message`  | ----------- |
| `--cleanup=<mode>`  | ----------- |
| `strip`  | ----------- |
| `whitespace`  | ----------- |
| `verbatim`  | ----------- |
| `scissors`  | ----------- |
| `default`  | ----------- |
| `-e` `--edit`  | ----------- |
| `--no-edit`  | ----------- |
| `--amend`  | ----------- |
| `--no-post-rewrite`  | ----------- |
| `-i` `--include`  | ----------- |
| `-o` `--only`  | ----------- |
| `--pathspec-from-file=<file>`  | ----------- |
| `--pathspec-file-nul`  | ----------- |
| `-u[<mode>]` `--untracked-files[=<mode>]`  | ----------- |
| `-v` `--verbose`  | ----------- |
| `-q` `--quiet`  | Suppress commit summary message. |
| `--dry-run`  | does not make a real commit, but rather shows which paths are to be changed, which arent, and what is currently untracked  |
| `--status`  | Includes the output of `git status` in the commit message template when preparing the commit message (defaults to on) |
| `--no-status`  | Do not include the output of `git-status` in the commit message template when using an editor to prepare the default commit message. |
| `-S[<keyid>]` `--gpg-sign[=<keyid>]` `--no-gpg-sign`  | ----------- |
| `<pathspec>…​`  | commits the contents of the files that match the pathspec given, ignoring the changes already made to the index. These contents are also staged for the next commit on top of anything else previously staged |

## Additional points

<!-- Info on additional points if necessary -->
* Using the `-m` flag allows you to add a 50 character title to the commit. Not using `-m` will open an editor after the commit, allowing you to add a title and description body to the commit.

## How To Write A __GOOD__ and __READABLE__ Commit Message

Answer the question: "What does the commit do?"

## Basic Workflow

* How to use this
* one step at a time
  * additional information related to the previous step
    > `code related to step mentioned above.`
