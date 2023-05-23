# `git`

## Terminology.

## Common Commands

```sh
# Clone remote repository into a folder matching the repository name in the current working directory.
git checkout <repo-url>

# List branches.
git branch

# Delete branch locally.
git branch -d <branch-name>

# Delete brnach on the remote.
git push origin -d <branch-name>

# Stage the files in the current directory for commit.
git add .

# Git message to diplay when running `git commit` without the `-m` flag. <git-message-file> often named `.gitmessage`
git config commit.template <git-message-file>

# Commit.
git commit

# Push. <remote name> is usually origin by default.
git push <remote-name> <branch-name>

# Push all local branches listed by `git branch`.
git push --all <remote-name>
```
