# Add All

## Add All

```shell
git add .
```

## Add All Include Removed Files

```shell
git add -A .
git add --all .
```

* Tips

  ```shell
  $ git add .
  warning: You ran 'git add' with neither '-A (--all)' or '--ignore-removal',
  whose behaviour will change in Git 2.0 with respect to paths you removed.
  Paths like 'Datetime/ISO8601/README.md' that are
  removed from your working tree are ignored with this version of Git.

  * 'git add --ignore-removal <pathspec>', which is the current default,
    ignores paths you removed from your working tree.

  * 'git add --all <pathspec>' will let you also record the removals.

  Run 'git status' to check the paths you removed from your working tree.
  ```

## References

