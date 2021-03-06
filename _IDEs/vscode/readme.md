## VS Code

These are the settings that I am using in Visual Studio Code.

Complete file is included [here](./settings.md).


- Status bar background color in debug mode to be the quite the same as the theme that I am currently like (Pines):
  ```json
  "workbench.colorCustomizations": {
    "statusBar.debuggingBackground": "#223449",
  }
  ```
  Meanwhile, additional customizations related to status bar look were included. Again, check out the [complete settings](./settings.md) for details.

- Initially, I disabled the "fake" closing parens comments using:
  ```json
  "dart.closingLabels": false
  ```
  but later I reenabled them with a not-so-distracting foreground color, disabled the built-in `editor.matchBrackets`, and using the [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2) extension.
  The result is also in the [settings](./settings.md) page.
- Increased the allowed length of the line (considered by `dartfmt`) using:
  ```json
  "dart.lineLength": 100
  ```
- Default values used by Flutter generator:
  ```json
  "dart.flutterCreateIOSLanguage": "swift",
  "dart.flutterCreateOrganization": "tech.vision8",
  ```
- Handy keyboard shortcuts:
  - General ones:
    - `cmd + alt + 1` for Explorer view
    - `cmd + alt + 2` for Search view
    - `cmd + alt + 3` for SCM view
    - `cmd + alt + 4` for Debug view
    - `cmd + alt + 5` for Extensions view
    - `cmd + alt + d` for Debug console
    - `cmd + alt + z` for status bar showing toggle
  - IDEA like ones:
    - `cmd + y` for deleting the current line
    - `cmd + d` for duplicating the current line
  
  The concrete settings as stored in `keybindings.json`:
  ```json
  [
    {
        "key": "alt+cmd+1",
        "command": "workbench.view.explorer"
    },
    {
        "key": "alt+cmd+2",
        "command": "workbench.view.search"
    },
    {
        "key": "alt+cmd+3",
        "command": "workbench.view.scm"
    },
    {
        "key": "alt+cmd+4",
        "command": "workbench.view.debug"
    },
    {
        "key": "alt+cmd+5",
        "command": "workbench.view.extensions"
    },
    {
        "key": "alt+cmd+d",
        "command": "workbench.debug.action.toggleRepl"
    },
    {
        "key": "cmd+d",
        "command": "editor.action.copyLinesDownAction",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "cmd+y",
        "command": "editor.action.deleteLines",
        "when": "textInputFocus && !editorReadonly"
    },
   {
        "key": "alt+cmd+z",
        "command": "workbench.action.toggleStatusbarVisibility"
    },
  ]
  ```

