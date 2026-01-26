# Git

A complete Git & GitHub version-control practice repository with commands, workflows, and examples to help you learn and demonstrate everyday Git tasks.

## Table of contents

- [About](#about)
- [Repository structure](#repository-structure)
- [Quick start](#quick-start)
- [Common Git commands](#common-git-commands)
- [Recommended workflows](#recommended-workflows)
- [Exercises & examples](#exercises--examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## About

This repository is intended as a hands-on reference and practice playground for Git and GitHub. It collects useful commands, example workflows (feature branches, pull requests, rebasing, merging, resolving conflicts), and small exercises you can use to build confidence working with version control.

Whether you're new to Git or want a compact cheat sheet for daily use, this repo is structured to be practical and easy to follow.

## Repository structure

(Adapt this list if you add files or folders. Right now the repo is intentionally minimal; use these suggested folders as you expand.)

- README.md — this file
- docs/ — optional: deeper guides and explanations
- examples/ — optional: sample repositories, scripts, or exercises
- commands.md — optional: concise command reference
- workflows.md — optional: detailed workflows and diagrams

## Quick start

1. Clone the repository:
   git clone https://github.com/mdzaheerjk/Git.git

2. Inspect the repository:
   cd Git
   ls -la

3. Create a branch for a feature or exercise:
   git checkout -b feature/your-topic

4. Make changes, stage, and commit:
   git add .
   git commit -m "Add notes about X"

5. Push your branch and open a PR:
   git push -u origin feature/your-topic
   Open a pull request on GitHub for review.

## Common Git commands

Local repo basics
- git status — show changes
- git add <file|.> — stage changes
- git commit -m "message" — commit staged changes
- git diff — show unstaged changes
- git log --oneline --graph --decorate — compact history view

Branches
- git branch — list branches
- git branch <name> — create branch
- git checkout <branch> — switch branch
- git checkout -b <name> — create and switch

Sync with remote
- git fetch — fetch changes
- git pull — fetch + merge (or configure to rebase)
- git push — push commits

Undoing
- git restore <file> — discard working-tree changes
- git reset --soft HEAD~1 — undo last commit but keep changes staged
- git revert <commit> — create a new commit that undoes an earlier one

Stashing
- git stash — save work-in-progress
- git stash pop — reapply and remove from stash

Tagging and releases
- git tag -a v1.0.0 -m "v1.0.0" — create annotated tag
- git push origin v1.0.0 — publish tag

Inspecting
- git show <commit> — view a commit
- git blame <file> — see last change per line

## Recommended workflows

Feature-branch + Pull Request (recommended for teams)
1. Create a branch from main: git checkout -b feature/abc
2. Commit locally in logical steps.
3. Push the branch: git push -u origin feature/abc
4. Open a Pull Request on GitHub, request reviewers, and iterate with review comments.
5. Once approved, merge using the repository's preferred merge strategy (merge commit, squash, or rebase) and delete the branch.

Rebase workflow (clean linear history)
- Rebase your feature branch onto an updated main to keep history linear:
  git fetch origin
  git rebase origin/main
- Resolve conflicts, continue with git rebase --continue, then force-push if necessary:
  git push --force-with-lease

Handling conflicts
- When a conflict occurs, open the conflicting files, resolve markers, then:
  git add <resolved-file>
  git rebase --continue  (or git commit if merging)
- Use git status and git mergetool if helpful.

Undoing mistakes
- Prefer git revert for public shared history.
- Use git reset / git restore for local/private branches (careful with shared branches).

Squash commits before merging (optional)
- Interactive rebase to squash:
  git rebase -i origin/main
- Clean commits make history easier to read.

## Exercises & examples

Consider adding short exercises such as:
- Create a feature branch, implement a tiny change, open PR, ask for review, then merge.
- Simulate a conflict: Two branches edit the same line, practice resolving it.
- Practice rebasing a topic branch on an updated main.
- Create annotated tags and produce a changelog from tags.

You can add example solutions under an examples/ folder and short step-by-step guides in docs/.

## Contributing

Contributions and improvements are welcome.

- Fork the repo and create a branch for your changes.
- Follow the branch naming convention: feature/..., fix/..., docs/...
- Open a pull request describing your changes.
- Keep commits small and focused; document major changes in the PR description.

If you want, I can add a CONTRIBUTING.md file or set up issue and PR templates.

## License

This repository is licensed under the MIT License. See the LICENSE file for details.

## Contact

Maintainer: mdzaheerjk
- GitHub: https://github.com/mdzaheerjk

If you'd like, I can commit this README to the repository (push to main or create a branch and open a PR). Let me know how you'd like me to proceed.
