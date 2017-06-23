---
title: Tmux iTerm copy
tags: mac-tricks
---

#### Enable copy function in iTerm when using tmux
Default copying within tmux sessions is done using tmux key
bindings. But if we want to copy and use it elsewhere the regular mac
cmd+c and cmd+v doesn't work.

Inorder to make copy work within iTerm tmux session, you need to enable "Application in
terminal may access clipboard" in iTerm preferences > General
settings. After this setting enabled you can use Mac's cmd+c (copy) and
cmd+v (paste).
![enable-clipboard-iterm-tmux](/assets/iterm-tmux-copy.png)
