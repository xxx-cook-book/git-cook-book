# .bumpversion.cfg

##  .bumpversion.cfg

```
[bumpversion]
files = setup.py
commit = True
tag = True
current_version = 0.0.0
```

* files = setup.py

  * Files to change (default: [])

  * Can't have comment such as

    ```
    files = setup.py  # Files to change (default: [])
    ```

    * Above will try to change current_version in such files

      ```
      [<bumpversion.ConfiguredFile:setup.py>, <bumpversion.ConfiguredFile:>, <bumpversion.ConfiguredFile:#>, <bumpversion.ConfiguredFile:Files>, <bumpversion.ConfiguredFile:to>, <bumpversion.ConfiguredFile:change>, <bumpversion.ConfiguredFile:(default:>, <bumpversion.ConfiguredFile:[])>]
      ```

  * files =' configuration is will be deprecated, please use [bumpversion:file:...]

    ```
    [bumpversion]
    commit = True
    tag = True
    current_version = 0.0.0

    [bumpversion:file:setup.py]
    ```

## Installation

```shell
pip install bumpversion -U
or
pip install bumpversion --upgrade 
```

## Usage

* ``bumpversion [options] part [file]`` 

  * `part` (required)

    * The part of the version to increase, e.g. `minor`

      ```python
      In [10]: from versions import Version

      In [11]: v = Version.parse('1.2.3')

      In [12]: v.major, v.minor, a.patch
      Out[12]: (1, 2, 3)
      ```

  * `[file]` **default: none** (optional)

    * The file that will be modified


* Bump and Create Commit

  ```shell
  bumpversion patch --commit
  ```

* Bump and Create Tag

  ```shell
  bumpversion patch --commit --tag
  ```


## Configuration

```
$ bumpversion --help
usage: bumpversion [-h] [--config-file FILE] [--verbose] [--list]
                   [--allow-dirty] [--parse REGEX] [--serialize FORMAT]
                   [--search SEARCH] [--replace REPLACE]
                   [--current-version VERSION] [--dry-run] --new-version
                   VERSION [--commit | --no-commit] [--tag | --no-tag]
                   [--tag-name TAG_NAME] [--message COMMIT_MSG]
                   part [file [file ...]]

bumpversion: v0.5.3 (using Python v2.7.5)

positional arguments:
  part                  Part of the version to be bumped.
  file                  Files to change (default: [])

optional arguments:
  -h, --help            show this help message and exit
  --config-file FILE    Config file to read most of the variables from
                        (default: .bumpversion.cfg)
  --verbose             Print verbose logging to stderr (default: 0)
  --list                List machine readable information (default: False)
  --allow-dirty         Don't abort if working directory is dirty (default:
                        False)
  --parse REGEX         Regex parsing the version string (default:
                        (?P<major>\d+)\.(?P<minor>\d+)\.(?P<patch>\d+))
  --serialize FORMAT    How to format what is parsed back to a version
                        (default: ['{major}.{minor}.{patch}'])
  --search SEARCH       Template for complete string to search (default:
                        {current_version})
  --replace REPLACE     Template for complete string to replace (default:
                        {new_version})
  --current-version VERSION
                        Version that needs to be updated (default: None)
  --dry-run, -n         Don't write any files, just pretend. (default: False)
  --new-version VERSION
                        New version that should be in the files (default:
                        None)
  --commit              Commit to version control (default: False)
  --no-commit           Do not commit to version control
  --tag                 Create a tag in version control (default: False)
  --no-tag              Do not create a tag in version control
  --tag-name TAG_NAME   Tag name (only works with --tag) (default:
                        v{new_version})
  --message COMMIT_MSG, -m COMMIT_MSG
                        Commit message (default: Bump version:
                        {current_version} → {new_version})
```

## References

[1] peritus@github, [bumpversion — Version-bump your software with a single command](https://github.com/peritus/bumpversion)