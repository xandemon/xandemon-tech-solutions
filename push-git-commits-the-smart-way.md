# Push git commits the smart way

Don't you get bored of always running `git add .`, `git commit -m 'message'`, and `git push origin`? Here's how you can do this the smart way with just one git command:

### Setting Up Git Alias

For this, we need to wrap these git commands into a single command using a git alias. To add an alias, we can run a `git config` command like below:

```
git config --global alias.acp '!f() { git add . && git commit -m "$@" && git push origin HEAD; }; f'
```

This command does several things:

1. Defines an alias `acp` that can be run like so: `git acp "commit message"`
2. Creates a function `f()`, which does the following:
   - Runs `git add .`
   - Runs `git commit -m "commit message"`
   - Runs `git push origin HEAD`, which will push to the current branch
3. Executes function `f`

**Usage Example**
`git acp "commit message"`

---

If you like manually staging changes and only want to commit and push changes at once, then you can do this:

```
git config --global alias.cp '!f() { git commit -m "$@" && git push origin HEAD; }; f'
```

**Usage Example**
`git acp "commit message"`

---

### Unsetting Git Alias

To unset an alias, we can use the `--unset` flag.
`git config --global --unset alias.alias_name`
