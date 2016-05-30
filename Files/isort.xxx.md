# .isort.cfg

##  .isort.cfg

```
# See the menu of settings available here:
#   https://github.com/timothycrosley/isort/wiki/isort-Settings

[settings]
indent='    '
line_length=200
lines_after_imports=2
skip=migrations
```

## isort.sh

```shell
#!/bin/bash

isort -rc .  # work
isort -rc -sp . .  # work
isort -rc -sp .isort.cfg .  # not work
isort -rc -sp ./.isort.cfg .  # work
```

## Usage

* See [iSort Imports](https://xxx-cook-book.gitbooks.io/python-cook-book/content/Import/iSortImports.html)

## References

[1] isort@TT4IT, [isort — A Python utility / library to sort imports](http://tt4it.com/resources/discuss/2302/)