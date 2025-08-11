@"
# Editing Files

## Overview
This section focuses on using popular text editors in the Linux terminal. You will learn how to edit files with both beginner-friendly and advanced tools, as well as practice Vim through its built-in tutorial.

---

## Topics Covered
1. **Nano** — A simple, user-friendly terminal text editor suitable for beginners.
2. **Vim** — A powerful and widely-used default text editor in Linux, known for its efficiency.
3. **Vimtutor** — An interactive educational tool for learning Vim commands and workflows.

---

## Section Summary
By the end of this section, you will be able to:
- Open and edit files in **Nano**
- Navigate, edit, and save files in **Vim**
- Practice Vim commands and modes using **Vimtutor**

---

## List of Learned Commands

### Nano
- `nano <filename>` — Open a file in Nano for editing  
- `Ctrl+O` — Save changes  
- `Ctrl+X` — Exit Nano  
- `Ctrl+K` — Cut selected text  
- `Ctrl+U` — Paste text  

### Vim
- `vim <filename>` — Open a file in Vim  
- `i` — Enter insert mode  
- `Esc` — Return to command mode  
- `:w` — Save changes  
- `:q` — Quit Vim  
- `:wq` — Save and quit  
- `u` — Undo the last change  
- `/pattern` — Search for text  

### Vimtutor
- `vimtutor` — Launch the Vim tutorial for step-by-step learning

---
"@ | Set-Content -Path "03_Editing_Files/README.md"
