# Copy Patches Across Branches

* Make sure you are on the branch you want apply the commit to.

  ```shell
  git checkout master
  ```

* Execute the following:

  ```shell
  git cherry-pick <commit-hash>
  ```

## References

[1] Rahul@StackOverflow, [What does cherry-picking a commit with git mean?](http://stackoverflow.com/questions/9339429/what-does-cherry-picking-a-commit-with-git-mean)