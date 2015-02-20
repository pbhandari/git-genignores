# git-genignores

A small program to automatically download the required gitignore file from the
@github/gitignores directory.

# Usage
```
Usage: git-genignores [OPTIONS] LANGUAGE
    -l, --list                       Check whether the server has that particular gitignore file.
        --[no-]capitalize            Don't auto capitalize.
    -s, --server SERVER              Query SERVER for the gitignore files.
    -p, --port PORT                  Connect to SERVER on PORT.
        --[no-]ssl                   Use SSL to connect to tne SERVER
    -f, --format FORMAT              The format used to query the SERVER for the files.
        --header FORMAT              The format string to give to the server.
        --footer FORMAT              The format string to give to the server.
    -h, --help                       Display this help.
```
**Note** `--help` doesn't work when calling this as `git genignores`  since git
tries to look for a man page for this.

# Installation
```sh
cd $SOME_DIR
curl --remote-name https://raw.githubusercontent.com/pbhandari/git-genignores/master/git-genignores
```

**Note**: Make sure that `$SOME_DIR` is in `$PATH` if you want to call this as
`git genignores`.

# Examples
```sh
# Print out gitignores for Ada, Perl and Ruby
git genignores Ada Perl Ruby

# Save the gitignores to a file
git genignores Python > .gitignore

# Check whether the gitignore for Perl and Python
# exists in the server
git genignores --list Perl Python
```

# TODO
 - [ ] Add tests to make my life easier.
 - [ ] Add an `--output-file` option.
 - [ ] Allow for configurations to be read from git's default config files
 - [ ] `--list` is a stupid name, change it to something sane
