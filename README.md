# git-genignores

A small program to automatically download the required gitignore file from the
@github/gitignores directory.

# Usage
`git genignores [-l|--list] LANGUAGE`

# Installation
```
cd $SOME_DIR
curl --remote-name https://raw.githubusercontent.com/pbhandari/git-genignores/master/git-genignores
```

**Note**: Make sure that `$SOME_DIR` is in `$PATH` if you want to call this as
`git genignores`.

# Examples
```
# Print out gitignores for Ada, Perl and Ruby
git genignores ada perl ruby

# Save the gitignores to a file
git genignores python > .gitignore

# Check whether the gitignore for Perl and Python
# exists in the server
git genignores --list perl python
```

# TODO
 - [x] Allow support for --list.
 - [ ] Add tests to make my life easier.
 - [ ] Add an --output-file option.
 - [ ] Allow downloads from places other than github's gitignores directory.
