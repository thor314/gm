# Git-Merkle (GM) 
![](https://img.shields.io/badge/made_by_cryptograthor-black?style=flat&logo=undertale&logoColor=hotpink)

Git submodules of all repos I've worked on since 2017. Why:
- it is aesthetically pleasing to have a merkle tree totem representing the sum total of my work
- to recursively sync subsections of my work, across N machines
- `rg`-ing through my work to find snippets
- landing point to show my work to others
- gm

[read more here](https://thork.net/posts/2024-01-31-git-merkle/)

## what makes this a merkle-tree
Every repo stores the last-seen commit hash from the leaves. State changes to my body of work at the leaves must also
update the path of intermediate nodes, up to the root (this repo). 

## how to use it
- recursively clone the tree
- set up to run a cron script that updates the tree (see `linux/.cron/git_merkle.fish`)
- don't work directly in the tree. Let the tree clone and sync from elsewhere, to reduce chance for annoying commit-hash merge conflicts or accidental commits. This does mean there will be some duplication of resources. 

## how you can do the same
first, get comfortable with using the `gh` commandline tool, and `git submodule` commands. I might recommend creating a
few `abbr`s (fish) or `alias`es (zsh/bash) to simplify the process of updating your submodule structure. Expect this to
take a few hours. 

Then take a look at the [script](https://github.com/thor314/.cron/blob/main/git_merkle.fish) I use to update this tree.
I don't expect to do work directly in my merkle tree, which risks me screwing with internal elements by accident, or
having to deal with recursive merge conflicts in the tree (bummer).

To edit stuff, clone an internal repo somewhere else, e.g., `projects` and `rust-playground` live in my `$HOME`, and
work on files from that location. Just let the merkle tree automatically do its thing.

