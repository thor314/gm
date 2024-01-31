# Git-Merkle (GM) 
Git submodules of all repos I've worked on since 2017. Why:
- it is aesthetically pleasing to maintain a merkle tree of my body of work
- to recursively sync subsections of my work, across N machines
- gm

## what makes this a merkle-tree
Every repo stores the last-seen commit hash from the leaves. State changes to my body of work at the leaves must also
update the path of intermediate nodes, up to the root (this repo). 

