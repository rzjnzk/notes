# `git`

## Terminology.

## Common Commands

### Show the working tree status.
```sh
git status
```

### Clone remote repository into a folder matching the repository name in the current working directory.
```sh
git clone ${repo_url}
```

### List branches.
```sh
git branch
```

### List only remote branches.
```sh
git branch -lr
```

### List only local branches.
```sh
git branch -l
```

### List all branches, including local and remote.
```sh
git branch -la
```

### Change current branch.
```sh
git checkout ${branch_name}
```

### Create and change current branch.
```sh
git checkout -b ${branch_name}
```

### Create a branch without changing the current branch.
```sh
git branch ${branch_name}
```

### Delete branch locally.
### Add the `-f` flag to force.
```sh
git branch -d ${branch_name}
```

### Delete branch on the remote.

Add the `-f` flag to force.

```sh
git push origin -d ${branch_name}
```

or

```sh
git push origin :${branch_name}
```

### Push current branch to different branch on the remote.

```sh
git push origin HEAD:${branch_name}
```

### Stage the files in the current directory for commit.

```sh
git add .
```

### Git message to display when running `git commit` without the `-m` flag. `${git_message_file}` is often named `.gitmessage`.

```sh
git config commit.template ${git_message_file}
```

### Commit.

```sh
git commit
```

### Push. <remote name> is usually origin by default.

```sh
git push ${remote_name} ${branch_name}
```

### Push all local branches listed by `git branch`.

```sh
git push --all ${remote_name}
```

### List all commits. 

Press `q` to exit.

```sh
git log
```

### List all commits containing a given word.

```sh
git log --grep="${word}"
```

--

### Show commits that contains the code, then you can: git show <commit_sha>.
```sh
git log -S "${search_str}"
```

### An even easier way to show matches right there on the spot.
```sh
git log -S "${search_str}" -p
```

### Same as above, except applied to all branches instead of the checked out branch.
```sh
git log -S "${search_str}" -p --all
```

### Limit your search to only specific files in a specific directory.
```sh
git log -S "${search_str}" -p -- "${file_glob}"
```

### Search for a regex.
```sh
git log -G "${regex}" -p
```

--

### Show the commit message that contains your search term, you can supply either a string or regular expression with the same flag.
```sh
git log --grep "${search_str}"
```

### Same as above, except applied to all branches instead of the checked out branch.
```sh
git log --grep "${search_str}" --all
```

--
