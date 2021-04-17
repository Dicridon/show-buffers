# Show Buffers
An Emacs major mode displaying all **user buffers** (buffers without leading "*" and space) in a side window.

# Description
`show-buffers` is similar to Emacs' built-in `buffer-menu-mode` activated by command `list-buffers`. The main difference is that `show-buffers` displays only user buffers (buffers with a backed file) in a side window. 

Unlike `buffer-menu-mode` in which the buffer list is static, the content in `show-buffers` window is updated dynamically when buffers are created or buffers are killed. Modified buffers are labeled with a "*".


# Use
Put the show-buffers.el in your emacs' load path and add `(require 'show-buffers)` to your `init.el` file.

# Customization
Following variables can be customized:
- `show-buffers-window-width`: default to 35
- `show-buffers-window-position`: `'right` and `'left` are available. Default to `'right`
- `show-buffers-refresh-interval`: how frequently (in seconds) should `show-buffers` window be refreshed. Default to 1.0 second.
- `show-buffers-follow-interval`: how frequently (in seconds) should `show-buffers` window points to the buffer currently focused. Default to 0.8 seconds.

# Keybindings
Several commands are available for buffer killing, saving and switching. However, these commands
are NOT intended to be used outside the `show-buffers` side window. Instead, please use following keybindings in the side window (just like `treemacs`).

- `r`: refresh the side window
- `k`: kill the buffer under the cursor
- `s`: save the buffer under the cursor
- `S`: save all modified buffers
- `RET`: display and switch to the buffer under the cursor
- `q`: close the `show-buffers` side window
