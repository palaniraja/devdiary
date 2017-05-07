##TMUX 

* Default prefix : Ctrl-b 
* My Prefix: ` (backtick)

```
+-----------------------------+--------------------------------------------+
| tmux new -s adb             | Open a new session named "adb"             |
| <prefix> d                  | detach session                             |
| tmux attach -t adb          | attached session named "adb"               |
| tmux set -g mode-keys vi    | enable vi key to switch between panes      |
| <prefix> w                  | list windows in session                    |
| <prefix> "                  | horizontal split                           |
| <prefix> %                  | vertical split                             |
| <prefix> n or p             | cycle next/previous window                 |
| <prefix> ,                  | name a window                              |
| <prefix> f                  | find a window                              |
| tmux kill-session -t myname | kill session                               |
| tmux ls                     | list sessions                              |
| prefix [                    | to search                                  |
| q                           | quit search?                               |
| prefix z                    | Zoom window                                |
| prefix ctrl space           | to select text                             |
| prefix [                    | start, and end                             |
| Alt+w                       | copy                                       |
| ]                           | paste                                      |
| prefix [                    | and use arrowkeys/scroll (as page up/down) |
| Ctrl c                      | to back to normal mode                     |
| prefix c                    | to create a new window                     |
| prefix &                    | kill/close a window                        |
+-----------------------------+--------------------------------------------+
```




#### Links
https://gist.github.com/MohamedAlaa/2961058