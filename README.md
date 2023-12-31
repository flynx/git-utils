# git-utlis

This package provides a set of git _meta-porcelain_ commands to manage 
a work tree with multiple git repositories.

Provided commands:
- `git listall`  
  List repositories in tree.
- `git cloneall FILE`  
  Clone all repositories in file
- `git pullall`  
  Pull changes for all repositories in tree


These enable setting up and maintaining mutiple development machines with
a number of git repositories.

## Workflow

In a tree with multiple git repositories:
- to pull external changes to all repositories in a tree:
  ```shell
  $ git pullall -r
  ```
- to create the same env on a different computer:
  ```shell
  $ git listall -o -r > repos.lst
  ```
  move the `repos.lst` to the target machine and:
  ```shell
  $ git cloneall repos.lst
  ```


## License

[BSD 3-Clause License](./LICENSE)

Copyright (c) 2023, Alex A. Naanou,  
All rights reserved.


<!-- vim:set ts=4 sw=4 spell : -->
