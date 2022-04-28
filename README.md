<!-- markdownlint-disable no-inline-html -->

# Japanese Morpheme Handler

Morpheme based cursor movement in Japanese text for [VS Code](https://code.visualstudio.com).


## How to activate the logic?

Just install the extension. Doing so changes the action for the keybindings
below (on macOS, use <kbd>⌥Option</kbd> instead of <kbd>Ctrl</kbd>):

- <kbd>Ctrl</kbd>+<kbd>Right</kbd>
- <kbd>Ctrl</kbd>+<kbd>Left</kbd>
- <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Right</kbd>
- <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Left</kbd>
- <kbd>Ctrl</kbd>+<kbd>Delete</kbd>
- <kbd>Ctrl</kbd>+<kbd>Backspace</kbd>

Although not visible in command platte, these actions are implemented as
commands so that you can reassign any key combinations to them.
The table below shows all available commands and their default keybindings:

| Command                                          | Default Keybinding (except macOS)                 | Default keybinding (for macOS)                      |
| ------------------------------------------------ | ------------------------------------------------- | --------------------------------------------------- |
| `morphemeWordHandler.cursorWordEndLeft`          | [*1]                                              | [*1]                                                |
| `morphemeWordHandler.cursorWordEndLeftSelect`    | [*1]                                              | [*1]                                                |
| `morphemeWordHandler.cursorWordEndRight`         | <kbd>Ctrl</kbd>+<kbd>Right</kbd>                  | <kbd>Option</kbd>+<kbd>Right</kbd>                  |
| `morphemeWordHandler.cursorWordEndRightSelect`   | <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Right</kbd> | <kbd>Option</kbd>+<kbd>Shift</kbd>+<kbd>Right</kbd> |
| `morphemeWordHandler.cursorWordStartLeft`        | <kbd>Ctrl</kbd>+<kbd>Left</kbd>                   | <kbd>Option</kbd>+<kbd>Left</kbd>                   |
| `morphemeWordHandler.cursorWordStartLeftSelect`  | <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Left</kbd>  | <kbd>Option</kbd>+<kbd>Shift</kbd>+<kbd>Left</kbd>  |
| `morphemeWordHandler.cursorWordStartRight`       | [*1]                                              | [*1]                                                |
| `morphemeWordHandler.cursorWordStartRightSelect` | [*1]                                              | [*1]                                                |
| `morphemeWordHandler.deleteWordEndLeft`          | [*1]                                              | [*1]                                                |
| `morphemeWordHandler.deleteWordEndRight`         | <kbd>Ctrl</kbd>+<kbd>Delete</kbd>                 | <kbd>Option</kbd>+<kbd>Delete</kbd>                 |
| `morphemeWordHandler.deleteWordStartLeft`        | <kbd>Ctrl</kbd>+<kbd>Backspace</kbd>              | <kbd>Option</kbd>+<kbd>Backspace</kbd>              |
| `morphemeWordHandler.deleteWordStartRight`       | [*1]                                              | [*1]                                                |

- [*1] <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>9</kbd> is assigned
  for those commands so that they will appear in the Keyboard Shortcuts
  editor of VSCode. If you want to use those commands, please reassign
  other keybinding to them.

## What's the difference from the original?

With the original logic, pressing <kbd>Ctrl</kbd>+<kbd>Right</kbd> while the
cursor is at the beginning of a chunk of Japanese characters will move the
cursor to the end of it.

![Original cursor movement](images/japanese-word-handler-vanilla.gif)

With this extension, on the other hand, the cursor will stop at each place
where the Japanese character type (Hiragana, Katakana, ...) changes.

![Improved cursor movement](images/japanese-word-handler.gif)

## Known limitations

As of VSCode 1.37.0, extension cannot override word related actions below:

- Word selection on double click
- Automatic highlight of a word at where the cursor is
- 'Match Whole Word' option of text search

## Issue report

Please visit the
[project's GitHub page](https://github.com/sgryjp/japanese-word-handler)
and report it.

**Enjoy!**
