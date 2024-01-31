# Git-Merkle (GM) 
Git submodules of all repos I've worked on since 2017. Why:
- it is aesthetically pleasing to maintain a merkle tree of my body of work
- to recursively sync subsections of my work, across N machines
- `rg`-ing through my work to find snippets
- landing point to show my work to others
- gm

## what makes this a merkle-tree
Every repo stores the last-seen commit hash from the leaves. State changes to my body of work at the leaves must also
update the path of intermediate nodes, up to the root (this repo). 

## how to use it
- recursively clone the tree
- set up to run a cron script that updates the tree (see `linux/.cron/git_merkle.fish`)
- don't work directly in the tree. Let the tree clone and sync from elsewhere, to reduce chance for annoying commit-hash merge conflicts or accidental commits. This does mean there will be some duplication of resources. 
