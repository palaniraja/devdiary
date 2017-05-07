## VI & Emacs Reference card for common tasks
```
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Action                       | Vim                                                 | Emacs                                                          |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Open a file                  | vi filename _or_ :o filename                        | emacs filename                                                 |
| Save                         | :w                                                  | C-x C-s                                                        |
| Exit                         | :q                                                  | C-x C-c                                                        |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Move Left Right Up Down      | h l k j                                             | Arrow keys or C-b C-f C-n C-p                                  |
| Move word Forward Backward   | w b _or_ W B                                        | M-f M-b                                                        |
| Move to starting of the line | 0                                                   | C-a                                                            |
| Move to end of the line      | $                                                   | C-e                                                            |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Undo                         | u                                                   | C-_                                                            |
| Redo                         | Ctrl + r                                            | Something other than undo and C-_ (same undo)                  |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Cut                          | dw                                                  | C-w                                                            |
| Copy selected text           | y                                                   | M-w                                                            |
| Paste                        | p                                                   | C-y                                                            |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Select                       | v _then movement commands_                          | C-Space  _and_ movement keys                                   |
| Select word                  | vw _or_ vW                                          | C-Space _and_ M-f _or_ M-b                                     |
| Select line                  | V                                                   | C-a C-Space C-e                                                |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Goto 1st line                | gg                                                  | Esc-<                                                          |
| Goto end of file             | G                                                   | Esc->                                                          |
| Goto line n                  | G _n_                                               | M-g g _n_                                                      |
| Page up                      | Ctrl + b                                            | Esc-v                                                          |
| Page down                    | Ctrl + f                                            | C-v                                                            |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Cursor Top of screen         | H                                                   |                                                                |
| Cursor Middle of screen      | M                                                   |                                                                |
| Cursor End of screen         | L                                                   |                                                                |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
| Find                         | /search_string _and_ n _or_ N to move next instance | C-s search_string then cycle instances with C-s                |
| Find Backwards               | ?search_string _and_ n _or_ N to move next instance | C-r search_string then cycle instances with C-r                |
| Find and replace             | :s/old/new/g                                        | Esc-% _enter_ search_string _enter_ replace_string then y or n |
+------------------------------+-----------------------------------------------------+----------------------------------------------------------------+
```

#### Links

[Vim Cheat Sheet](https://vim.rtorr.com/)
[Emacs Cheat Sheet](https://ccrma.stanford.edu/guides/package/emacs/emacs.html)

alias emacs="/usr/local/Cellar/emacs/25.1/Emacs.app/Contents/MacOS/Emacs -nw"