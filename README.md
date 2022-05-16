# husky

> Modern native Git hooks made easy
Husky improves your commits and more 🐶 *woof!*

# Install

```
npm install
```

# Usage

Make a commit:

```sh
git commit -m "commit message"
# `pre-commit` hook will run to lint and prettify all staged files
# `commit-msg` hook will run to test if the commit message is matching the required pattern
# commit will be successful if both the above hooks returns true
```

push the changes:

```sh
git push
# `pre-push` hook will run to test if the branch name is matching the required pattern
# push will be successful if above hook returns true
```

# Documentation

https://typicode.github.io/husky