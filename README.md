# Neonote
A C++/ncurses terminal application for Markdown-style notes, task management and calendar entries, built as a Western University CS3307B team project.

## About this fork
This is my fork of the CS3307B team project at Western University. My main contribution was implementing the `Task` and `TaskManager` components. I also contributed to autosave, lightweight text formatting, and the Makefile.

The original team repository is [gdonlol/neonote](https://github.com/gdonlol/neonote). The original contributors and commit history are retained.

## How to run
Clone the repository.

```
https://github.com/Zheizh/neonote.git
```

Navigate to project directory in your terminal and use `make` to compile the program or `make run` to compile and run.

- The compiled binary will be located in the `bin/` folder.
- If the `bin/` directory doesn’t exist, `make` will automatically create it.

## Dependencies
Neonote relies on the following dependencies for proper compilation and execution.

1. `g++` (GCC)
2. **ncurses Library**
- Used for terminal-based UI rendering.
- Install commands for common Linux distributions:
- 2.1. Debian/Ubuntu:
```
sudo apt install libncurses5-dev libncursesw5-dev
```
- 2.2. Arch Linux:
```
sudo pacman -S ncurses
```
- 2.3. Fedora/RHEL:
```
sudo dnf install ncurses-devel
```
3. **GNU Make**
- Used to build the project using the provided `Makefile`.
- Install commands:
- 3.1. Debian/Ubuntu:
```
sudo apt install make
```
- 3.2. Arch Linux:
```
sudo pacman -S make
```
- 3.3. Fedora/RHEL:
```
sudo dnf install make
```

## Course project
Neonote was developed by CS3307B Group 14 at Western University. It brings note editing, task management and calendar features into a keyboard-driven terminal interface.

The original course brief targeted a virtual Raspberry Pi environment and did not require a physical kit.

## Features
- Markdown editing
- Keyboard user-centric, efficient keybinds for everything
- Kanban board todo list for productivity
- Calendars for event planning
- Interface for list of pages on sidebar

## Keybinds Guide
This guide provides an overview of the keybindings available in the terminal editor, covering both content editing and sidebar navigation.

1. **Main Menu Navigation**
- Arrow Up (↑) or `k` - Moves up the menu options.
- Arrow Down (↓) or `j` - Moves down the menu options.
- Enter (⏎) or `\n` - Selects the currently highlighted menu option (either "my notes" or "exit").

2. **Content Editing Mode**
- Arrow Keys (↑, ↓, ←, →) - Move the cursor up, down, left, or right.
- Backspace (⌫) - Deletes the character to the left of the cursor.
- Enter (⏎) - Inserts a new line at the current cursor position.
- `Ctrl + S` - Saves the current file.
- `Ctrl + Q` - Saves and exits the editor.
- `Ctrl + B` - Inserts ** (bold formatting marker).
- `Ctrl + I` - Inserts * (italic formatting marker).
- `Ctrl + O` / `Ctrl + D` - Switches focus to the sidebar.
- `Ctrl + N` - Makes a new file.
- `Ctrl + ]` - Move the cursor to the start of the previous word.
- `Ctrl + \` - Skip to the next word.
- Printable Characters (`A-Z`, `0-9`, `Symbols`) - Inserts the typed character at the cursor position.

3. **Sidebar Navigation Mode**
- Arrow Up (↑) - Moves up the file list.
- Arrow Down (↓) - Moves down the file list.
- Enter (⏎) - Loads the selected file or page into the editor.
- `Ctrl + O` / `Ctrl + D` - Switches focus back to content editing.
- `Ctrl + R` - Rename a file (click enter to confirm after typing in new name).
- `Ctrl + T` - Create a new task for the kanban board (click enter to confirm after typing in new name).
- `Ctrl + P` - Move an existing task into a new category (to do, in progress or done).

4. **Cursor and Scroll Adjustments**
- Cursor movement is restricted within the text bounds.
- Scrolling occurs automatically when the cursor moves beyond the visible area.
