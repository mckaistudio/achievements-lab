# Git and GitHub quick reference

A beginner-friendly reference in English and Roman Urdu. Use a disposable practice repository, not an important project, while learning.

## GitHub without a terminal

- **Repository:** A project and its files. Roman Urdu: project ki files rakhne ki jagah.
- **Fork:** Your own copy of someone else's repository. Roman Urdu: kisi project ki apne account mein copy.
- **Branch:** An independent line of work. Roman Urdu: asal project ko chhere baghair alag jagah par kaam.
- **Commit:** A saved record of a change. Roman Urdu: tabdeeli ka saved record.
- **Pull request:** A request to review and integrate changes. Roman Urdu: apni tabdeeli check aur merge karwane ki request.
- **Merge:** Integrate approved changes into a target branch. Roman Urdu: approved tabdeeliyan main branch mein shamil karna.

## Safe terminal practice

First install Git from https://git-scm.com/ if it is not installed. Open Git Bash or a terminal. The following exercise uses a new local folder and does not push anything to GitHub.

```sh
mkdir github-practice
cd github-practice
git init
git status
git switch -c practice/first-note
```

Create a file named `notes.txt` in this folder using a text editor. Add a short practice note and save it. Then run:

```sh
git add notes.txt
git diff --cached
git commit -m "docs: add first practice note"
git status
git log -1 --oneline
```

If Git asks for an author identity, configure a name and an email for this practice repository only using `git config user.name` and `git config user.email` with your own chosen values. GitHub provides a no-reply address in email settings if you prefer not to publish your personal email.

Expected result: one commit appears in the log and the working tree is clean. Nothing is uploaded by these commands.

## Common mistakes

- **Not a git repository:** Check that your terminal is inside the practice folder; run `git status` again.
- **Nothing to commit:** Save your editor file and use `git status` to check whether Git sees the change.
- **Wrong branch:** Run `git branch --show-current` before editing or committing.
- **Permission denied on GitHub:** Confirm your account has access to the target repository. Do not share a password or token to resolve this.
- **Merge conflict:** Do not force-push or discard someone else's edits. Inspect the conflicting lines and ask for review.

## Before opening a pull request

- Check the target repository and target branch.
- Review the actual changed files.
- Explain what changed, why, and what you tested.
- Remove any private information and credentials.
- Credit only real contributors.

Need help? Ask in [Discussions](https://github.com/mckaistudio/achievements-lab/discussions). For a reproducible documentation problem, use [Issues](https://github.com/mckaistudio/achievements-lab/issues).

Official references: [Git documentation](https://git-scm.com/docs), [GitHub Docs](https://docs.github.com/).
