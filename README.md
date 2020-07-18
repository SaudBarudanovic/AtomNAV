# AtomNAV
An Atom keymap snippet that enables you to navigate through, select, and delete (both with backspace and delete) subwords (works with camelCase, snake_case, kebab-case and PascalCase)

### Add the following snippet to your Atom's keymap.cson file:
```
'.editor':
  'ctrl-backspace': 'editor:delete-to-beginning-of-subword'
  'ctrl-delete': 'editor:delete-to-end-of-subword'
  'ctrl-right': 'editor:move-to-next-subword-boundary'
  'ctrl-left': 'editor:move-to-previous-subword-boundary'
  'ctrl-shift-right': 'editor:select-to-next-subword-boundary'
  'ctrl-shift-left': 'editor:select-to-previous-subword-boundary'
```

# VSCode
Achieve the same functionality in VSCode by editing your "keybindings.json" file, and adding the following keymaps:
## Windows:
```
[
    { "key": "ctrl+right",          "command": "cursorWordPartRight",
        "when": "textInputFocus" },
    { "key": "ctrl+shift+right",    "command": "cursorWordPartRightSelect",
        "when": "textInputFocus" },
    { "key": "ctrl+left",           "command": "cursorWordPartStartLeft",
        "when": "textInputFocus" },
    { "key": "ctrl+shift+left",     "command": "cursorWordPartStartLeftSelect",
        "when": "textInputFocus" },
    { "key": "ctrl+backspace",      "command": "deleteWordPartLeft",
        "when": "textInputFocus && !editorReadonly" },
    { "key": "ctrl+delete",         "command": "deleteWordPartRight",
        "when": "textInputFocus && !editorReadonly" }
]
```
## macOS:
```
[
    { "key": "cmd+right",          "command": "cursorWordPartRight",
        "when": "textInputFocus" },
    { "key": "cmd+shift+right",    "command": "cursorWordPartRightSelect",
        "when": "textInputFocus" },
    { "key": "cmd+left",           "command": "cursorWordPartStartLeft",
        "when": "textInputFocus" },
    { "key": "cmd+shift+left",     "command": "cursorWordPartStartLeftSelect",
        "when": "textInputFocus" },
    { "key": "cmd+backspace",      "command": "deleteWordPartLeft",
        "when": "textInputFocus && !editorReadonly" },
    { "key": "cmd+delete",         "command": "deleteWordPartRight",
        "when": "textInputFocus && !editorReadonly" }
]
```
### That's it! Enjoy your subword ctrl navigations and deletions!
