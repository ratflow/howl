# Changelog

## In master (unreleased)

- Avoid having the readline grow and shrink as much, which is annoying since it
requires the eyes to move up and down. Now the readline will only grow during
one read() invocation, and will keep the same fixed size regardless of the
amount of items in the completion list.

- Added howl.clipboard, new module for handling multiple clipboard items.

- Removed fuzzy matching. It was noisy, and added little value.

- Sped up chunk.text access, resulting in a giant speed-up for buffer-grep and
buffer-structure commands when working with large files.

### Bugs

- Completion popup now closes upon entering a non-character

- Buffer grep fixed for buffers with empty lines

- Byte code compilation no longers requires a $DISPLAY

- Overly long lines in the readline are now shortened to avoid horizontal
scrolling.

- `buffer-replace` command now works correctly with an empty replacement string.

### VI bundle

- Fix pasting of line block yanks (i.e. <y><y>/<Y>/<d><d>)
- Fix count handling for yank
- Fix <y><y> to yank current line correctly
- Support '<' and '>' in visual mode

### Command name changes

In order to streamline the naming of commands, the below commands have been
renamed:

* toggle-fullscreen -> window-toggle-fullscreen
* toggle-maximized -> window-toggle-maximized

* search-forward -> buffer-search-forward
* repeat-search -> buffer-repeat-search
* replace -> buffer-replace
* replace-pattern -> buffer-replace-pattern
* reload-buffer -> buffer-reload

* mode-set -> set-for-mode
* buffer-set -> set-for-buffer

* new-view-above -> view-new-above
* new-view-below -> view-new-below
* new-view-left-of -> view-new-left-of
* new-view-right-of -> view-new-right-of

The old command names are still present and working, but are deprecated and will
be removed in a future release.

## 0.1.1 (2014-03-15)

- Fix incompatibility with older Gtk versions.

## 0.1 (2014-03-15)

First public release.