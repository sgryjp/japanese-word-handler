# Change Log

All notable changes to the "japanese-word-handler" extension will be
documented in this file.

The format is based on
[Keep a Changelog](http://keepachangelog.com/en/1.0.0/) this project adheres
to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

<!-- markdownlint-disable MD022 MD024 MD032 MD033 -->

## [Unreleased]

## [1.4.1] - 2021-11-06

### Fixed

- Now japanese-word-handler works on on desktop environments too
  (v1.4.0 works only on web environment) (#16)

## [1.4.0] - 2021-11-05

### Feature

- Now japanese-word-handler is a web extension so it can be used on `vscode.dev`

## [1.3.0] - 2021-10-02

### Feature

- Untrusted workspaces support

## [1.2.3] - 2021-08-15

### Fixed

- Now the extension can be used on non-desktop host (#11)

## [1.2.2] - 2020-11-06

### Fixed

- Update dependencies to suppress vulnerability warnings (affects developer only)

## [1.2.1] - 2020-04-29

### Fixed

- Now word deletion won't be triggered when user does not focus file editing window
  ([Issue #5](https://github.com/sgryjp/japanese-word-handler/issues/5))

## [1.2.0] - 2019-08-15

### Added

- New command `japaneseWordHandler.cursorWordEndLeft`
- New command `japaneseWordHandler.cursorWordEndLeftSelect`
- New command `japaneseWordHandler.cursorWordStartRight`
- New command `japaneseWordHandler.cursorWordStartRightSelect`
- New command `japaneseWordHandler.deleteWordEndLeft`
- New command `japaneseWordHandler.deleteWordStartRight`

### Change

- Change command names to match built-in commands (old names can be used for compatibility but will be removed in future):

  | Old Command Names                       | New Command Names                               |
  | --------------------------------------- | ----------------------------------------------- |
  | `extension.cursorNextWordEndJa`         | `japaneseWordHandler.cursorWordEndRight`        |
  | `extension.cursorNextWordEndSelectJa`   | `japaneseWordHandler.cursorWordEndRightSelect`  |
  | `extension.cursorPrevWordStartJa`       | `japaneseWordHandler.cursorWordStartLeft`       |
  | `extension.cursorPrevWordStartSelectJa` | `japaneseWordHandler.cursorWordStartLeftSelect` |
  | `extension.deleteWordRight`             | `japaneseWordHandler.deleteWordEndRight`        |
  | `extension.deleteWordLeft`              | `japaneseWordHandler.deleteWordStartLeft`       |

## [1.1.1] - 2018-10-17

### Fixed

- Now scrolls the window so that the cursor is always visible except when there are multiple cursors

## [1.1.0] - 2018-09-24

### Added

- Multi-cursor support
- New command `extension.deleteWordRight` with keyboard shortcut <kbd>Ctrl+Delete</kbd>
- New command `extension.deleteWordLeft` with keyboard shortcut <kbd>Ctrl+Backspace</kbd>

## [1.0.0] - 2018-05-21

### Added

- Now respects VSCode's `editor.wordSeparators` configuration
  ([PR #2](https://github.com/sgryjp/japanese-word-handler/pull/2), contribution
  by [@tekezo](https://github.com/tekezo))

### Fixed

- Moving cursor with Ctrl+Left over whitespaces at start of a document fails
  ([Issue #3](https://github.com/sgryjp/japanese-word-handler/issues/3))

## [0.5.1] - 2018-04-19

### Fixed

- Doesn't work on macOS because of incorrect keybinding settings

## [0.5.0] - 2017-05-01

- Initial release
