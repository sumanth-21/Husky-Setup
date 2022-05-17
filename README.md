# husky

> Modern native Git hooks made easy

Husky is a tool that allows you to easily wrangle Git hooks and run the scripts you want at different stages of git commands.

You can use it to lint your commit messages, run tests, lint code, lint branch naming etc... when you commit or push. Husky supports all Git hooks.

# Install


Install dependencies with npm install.

```
npm install
```

# For MAC Users

Run the below commands to set Husky as executable:

```sh
chmod ug+x .husky/*
chmod ug+x .git/hooks/*
```

# Config

## Pre-Commit hook
> /.husky/pre-commit
> 
> /.lintstagedrc

Here 'lint-staged' is being used to lint the staged files. Lint config changes can be done in the lintstagedrc file.

## Commit Message hook
> /.husky/commit-msg

You can change the 'PATTERN' of your commit message as per your requirement in the commit-msg file.

## Pre-Push hook
> /.husky/pre-push

You can change the 'valid_branch_regex' in the pre-push file according to the desired branch name pattern to be followed.

# Usage

## Add your changes and Make a commit:

```sh
git add yourFiles
git commit -m "your commit message"
```

### 'pre-commit' hook

```sh
# `pre-commit` hook will execute to lint and prettify all the staged files
```

### 'commit-msg' hook

```sh
# `commit-msg` hook will execute to test if the commit message is matching the required pattern.
```
Your commit will be successful if both the above hooks returns true

## Push your changes

```sh
git push
```

### 'pre-push' hook

```sh
# `pre-push` hook will execute to test if the branch name is matching the required pattern
```
Your push will be successful if 'pre-push' hook returns true

# Documentation

https://typicode.github.io/husky
