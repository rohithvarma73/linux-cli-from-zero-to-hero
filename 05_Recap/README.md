# Recap

This section contains quick-reference cheat sheets for the two main text editors covered in this course: **GNU Nano** and **Vim**.

---

## 1. GNU Nano Cheat Sheet

**File Handling**
- `Ctrl+S` — Save current file  
- `Ctrl+O` — Offer to write file ("Save as")  
- `Ctrl+R` — Insert a file into current one  
- `Ctrl+X` — Close buffer, exit from nano  

**Editing**
- `Ctrl+K` — Cut current line into cutbuffer  
- `Alt+6` — Copy current line into cutbuffer  
- `Ctrl+U` — Paste contents of cutbuffer  
- `Alt+T` — Cut until end of buffer  
- `Ctrl+]` — Complete current word  
- `Alt+3` — Comment/uncomment line/region  
- `Alt+U` — Undo last action  
- `Alt+E` — Redo last undone action  

**Search and Replace**
- `Ctrl+Q` — Start backward search  
- `Ctrl+W` — Start forward search  
- `Alt+Q` — Find next occurrence backward  
- `Alt+W` — Find next occurrence forward  
- `Alt+R` — Start a replacing session  

**Deletion**
- `Ctrl+H` — Delete character before cursor  
- `Ctrl+D` — Delete character under cursor  
- `Alt+Bsp` — Delete word to the left  
- `Ctrl+Del` — Delete word to the right  
- `Alt+Del` — Delete current line  

**Operations**
- `Ctrl+T` — Execute some command  
- `Ctrl+J` — Justify paragraph or region  
- `Alt+J` — Justify entire buffer  
- `Alt+B` — Run a syntax check  
- `Alt+F` — Run a formatter/fixer/arranger  
- `Alt+:` — Start/stop recording of macro  
- `Alt+;` — Replay macro  

**Moving Around**
- `Ctrl+B` — One character backward  
- `Ctrl+F` — One character forward  
- `Ctrl+←` — One word backward  
- `Ctrl+→` — One word forward  
- `Ctrl+A` — To start of line  
- `Ctrl+E` — To end of line  
- `Ctrl+P` — One line up  
- `Ctrl+N` — One line down  
- `Ctrl+↑` — To previous block  
- `Ctrl+↓` — To next block  
- `Ctrl+Y` — One page up  
- `Ctrl+V` — One page down  
- `Alt+\` — To top of buffer  
- `Alt+/` — To end of buffer  

**Special Movement**
- `Alt+G` — Go to specified line  
- `Alt+]` — Go to complementary bracket  
- `Alt+↑` — Scroll viewport up  
- `Alt+↓` — Scroll viewport down  
- `Alt+<` — Switch to preceding buffer  
- `Alt+>` — Switch to succeeding buffer  

**Information**
- `Ctrl+C` — Report cursor position  
- `Alt+D` — Report line/word/character count  
- `Ctrl+G` — Display help text  

**Various**
- `Alt+A` — Turn the mark on/off  
- `Tab` — Indent marked region  
- `Shift+Tab` — Unindent marked region  
- `Alt+V` — Enter next keystroke verbatim  
- `Alt+N` — Turn line numbers on/off  
- `Alt+P` — Turn visible whitespace on/off  
- `Alt+X` — Hide/unhide the help lines  
- `Ctrl+L` — Refresh the screen  

---

## 2. Vim Cheat Sheet

**Essentials: Cursor Movement (Normal/Visual Mode)**
- `h` `j` `k` `l` — Arrow keys  
- `w` / `b` — Next/previous word  
- `W` / `B` — Next/previous word (space-separated)  
- `e` / `ge` — Next/previous end of word  
- `0` / `$` — Start/end of line  
- `^` — First non-blank character of line  

**Editing Text**
- `i` / `a` — Start insert mode at/after cursor  
- `I` / `A` — Insert at start/end of line  
- `o` / `O` — Add blank line below/above  
- `Esc` — Exit insert mode  
- `d` / `dd` — Delete / delete line  
- `c` / `cc` — Change / change line  

**Operators**
- `d` — Delete  
- `c` — Change  
- `y` — Yank (copy)  
- `>` — Indent  
- `<` — Unindent  

**Marking Text**
- `v` — Visual mode  
- `V` — Visual line mode  
- `Ctrl+v` — Visual block mode  

**Clipboard**
- `yy` — Yank line  
- `p` / `P` — Paste after/before cursor  
- `x` / `X` — Delete character  

**Exiting**
- `:w` — Save  
- `:wq` — Save & quit  
- `:q` — Quit  
- `:q!` — Quit without saving  

**Search/Replace**
- `/pattern` — Search forward  
- `?pattern` — Search backward  
- `:%s/old/new/g` — Replace all  
- `:%s/old/new/gc` — Replace with confirmation  

**General**
- `u` — Undo  
- `Ctrl+r` — Redo  
- `.` — Repeat last command  

**Advanced: Movement**
- `Ctrl+d` — Half page down  
- `Ctrl+u` — Half page up  
- `}` / `{` — Next/previous paragraph  
- `gg` — Top of file  
- `G` — Bottom of file  

**Character Search**
- `f` / `F` — Find char forward/backward  
- `t` / `T` — Till char forward/backward  
- `;` / `,` — Repeat search  

**Visual Mode Movement**
- `O` — Other corner of block  
- `o` — Other end of marked area  

**Tabs and Splits**
- `:tabe` — New tab  
- `gt` / `gT` — Next/previous tab  
- `:vsp` — Vertical split  
- `Ctrl+ww` — Switch windows  

**Marks**
- `m{a-z}` — Set mark  
- `'{a-z}` — Jump to mark  

**Text Objects**
- `di(` — Delete inside parentheses  

---
"@ | Set-Content -Path "05_Recap/README.md"
