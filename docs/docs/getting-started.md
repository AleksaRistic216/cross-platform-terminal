# Getting Started

## First Launch

When Cross Platform Terminal opens, you'll see a single view (tab) named **View 1** with one terminal panel already open. The terminal starts in your home directory.

---

## Core Concepts

### Views

A **View** is a tab — a named workspace with its own independent panel layout. Think of it as a virtual desktop within the window.

- Create a new view: **Alt+T** (you'll be prompted to name it)
- Rename the active view: **Alt+R**
- Switch views by clicking the tab bar at the top, or right-click a tab for options

Views are automatically suspended when you switch away from them — terminal output is buffered, not lost. After several minutes of inactivity, a view is unloaded to disk to free memory. Clicking the tab restores it instantly.

### Widgets

A **Widget** is a panel inside a view. Cross Platform Terminal has two widget types:

- **Terminal** — a full PTY terminal with tab support
- **File Browser** — a filesystem navigator

Add widgets from the **Widgets** menu in the menu bar. You can have as many widgets as you like in a view, arranged by dragging their title bars to dock them next to each other.

### Docking

Widgets are docked using ImGui's docking system. To rearrange:

1. Drag a widget's title bar toward an edge of another widget until a blue drop target appears.
2. Release to dock it there.

To equalize an uneven layout: **Ctrl+Shift+Alt+L** (Redistribute Layout).

**View → Auto Layout Mode** decides what that produces, and where a newly opened
widget lands:

- **Side by Side** (default) — every widget in one even row.
- **Smart** — keep the arrangement the view has and only even out the pane sizes
  within it.

The explicit splits below (**Ctrl+Shift+G** / **Ctrl+Shift+F**) always go where
you asked, whichever mode is set.

To keep one panel out of that — a narrow file tree, a log pane you sized by hand
— pin it with the thumbtack button in its tab strip, or **Ctrl+Shift+Alt+P**. A
pinned panel keeps its size and its place, and the rest share out what is left.

---

## Working with Terminals

A terminal widget supports multiple tabs. With a terminal focused:

| What you want | How |
|---------------|-----|
| New tab in this panel | `Ctrl+Shift+T` |
| Split — new panel below | `Ctrl+Shift+G` |
| Split — new panel to the right | `Ctrl+Shift+F` |
| Close current tab | `Ctrl+Shift+W` |
| Zoom in / out | `Ctrl+Shift+=` / `Ctrl+Shift+-` |

Splits (**G** and **F**) open a new terminal widget docked adjacent to the current one and inherit the current working directory of the focused terminal.

---

## Navigating Without a Mouse

Once you have multiple panels open, use keyboard focus shortcuts to move between them:

| Direction | Shortcut |
|-----------|---------|
| Left | `Ctrl+Alt+Home` |
| Right | `Ctrl+Alt+End` |
| Up | `Ctrl+Alt+Page Up` |
| Down | `Ctrl+Alt+Page Down` |

To move a panel to a different position: `Ctrl+Shift+Alt+` + `Home/End/Page Up/Page Down`.  
To resize a panel: `Ctrl+Shift+Alt+` + `[ ] ; '`.

---

## Workflows

A Workflow is a named sequence of steps that can inject text or run a script into the focused terminal. Open the Workflow panel from the **Workflows** menu, define steps (Prepend text, Append text, Script, etc.), and trigger the workflow to have it type into your terminal automatically. This is useful for repetitive command sequences or environment setup.

---

## Settings

Open **Settings** from the menu bar to access:

- **About** — current version
- **Keyboard Shortcuts** — view and rebind all shortcuts
- **Terminal** — font size, shell, and other terminal options
