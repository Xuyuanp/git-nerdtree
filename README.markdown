The NERD Tree
=============

New Feature
----------

Add git status support for NERDTree.You can indicate a file's git status, quickly see which files you have staged, unstaged and modified, or deleted in your project without any extra work.

![Imgur](http://i.imgur.com/jSCwGjU.gif?1)

Indicators
----------

* `✭` / `*` : Untracked
* `✹` / `~` : Modified in the working tree
* `✚` / `+` : Staged in the index (Exclude Renamed status)
* `➜` / `»` : Renamed
* `═` / `=` : Unmerged
* `✖` / `-` : Deleted (This indicator can't be shown, as NERDTree doesn't display deleted files. I have no prefect idea to solve this problem currently.)
* `✗` / `×` : Dirty (Only for directory)
* `✔` / `ø` : Clean (Only for root directory)

**Option** `let g:NERDTreeUseSimpleIndicator = 1` to show the simple indicator.

Key mapping
-----------

As the same as [GitGutter](https://github.com/airblade/vim-gitgutter) plugin default.

* `]c` : Jump to next indicator
* `[c` : Jump to prev indicator

You can set `g:NERDTreeMapNextHunk` and `g:NERDTreeMapPrevHunk` variables to your prefer keys. e.g.

`let g:NERDTreeMapNextHunk = ",n"`

`let g:NERDTreeMapPrevHunk = ",p"`

Status Refresh
--------------

`Add`, `Delete`, `Move` and `Copy` actions through the `m` menu will refresh git status indicators automatically.

File modified, `stage` or `commit` actions through **vim-fugitive** plugin won't active the status refreshing, this is because that NERDTree itself doesn't support auto refreshing function. You should press `r` or `R` to refresh the tree view by yourself after these actions.

Note
----

It's **NOT** a plugin of NERDTree, but an enhance version.

More Info
=======

See details in https://github.com/scrooloose/nerdtree
