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
  $ git listall -r > repos.lst
  ```
  move the `repos.lst` to the target machine and:
  ```shell
  $ git cloneall repos.lst
  ```
- to update the repository list with new repos:
  ```shell
  $ git listall -r repos.lst >> repos.lst
  ```


## Tips
- It is convenient to manage `repos.lst` as symlinks to a unified directory and
  syncronize it between machines via someting like [syncthing](https://syncthing.net/)


## License

[BSD 3-Clause License](./LICENSE)

Copyright (c) 2023, Alex A. Naanou,  
All rights reserved.


<!-- vim:set ts=4 sw=4 spell : -->
