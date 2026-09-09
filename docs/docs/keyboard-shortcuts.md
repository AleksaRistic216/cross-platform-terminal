# Keyboard Shortcuts

All shortcuts are rebindable. To customize them, open **Settings → Keyboard Shortcuts** inside the app, or edit the config file directly — see [Customization](../customization.md).

---

## Views

| Action | Default |
|--------|---------|
| New View | `Alt+T` |
| Rename Active View | `Alt+R` |
| Redistribute Layout | `Ctrl+Shift+Alt+L` |

**Redistribute Layout** equalizes all dock node sizes in the active view, useful after docking many panels unevenly.

---

## Widget Navigation

Move keyboard focus between widgets without using the mouse.

| Action | Default |
|--------|---------|
| Focus Widget Left | `Ctrl+Alt+Home` |
| Focus Widget Right | `Ctrl+Alt+End` |
| Focus Widget Up | `Ctrl+Alt+Page Up` |
| Focus Widget Down | `Ctrl+Alt+Page Down` |

---

## Widget Management

| Action | Default |
|--------|---------|
| Close Focused Widget | `Ctrl+Shift+W` |
| Pin/Unpin Widget | `Ctrl+Shift+Alt+P` |
| Move Widget Left | `Ctrl+Shift+Alt+Home` |
| Move Widget Right | `Ctrl+Shift+Alt+End` |
| Move Widget Up | `Ctrl+Shift+Alt+Page Up` |
| Move Widget Down | `Ctrl+Shift+Alt+Page Down` |
| Shrink Widget Width | `Ctrl+Shift+Alt+[` |
| Grow Widget Width | `Ctrl+Shift+Alt+;` |
| Shrink Widget Height | `Ctrl+Shift+Alt+]` |
| Grow Widget Height | `Ctrl+Shift+Alt+'` |

**Pin/Unpin Widget** protects a deliberately sized panel — a narrow file tree on
the left, a log pane on the right — from the automatic re-layouts. A pinned
widget keeps its size and its slot when you Redistribute Layout or close a
sibling, and the move shortcuts neither move it nor displace it. Everything else
shares out the space that is left. Dragging and the resize shortcuts still work
on a pinned widget, so pinning is not a lock.

The same toggle is the thumbtack button in a panel's tab strip, next to the
maximize button. A pinned panel shows a filled blue thumbtack there, and a blue
dot beside its tab name.

---

## Terminal (when a terminal panel is focused)

| Action | Default |
|--------|---------|
| New Tab | `Ctrl+Shift+T` |
| New Terminal Below | `Ctrl+Shift+G` |
| New Terminal to the Right | `Ctrl+Shift+F` |
| Close Tab | `Ctrl+Shift+W` |
| Zoom In | `Ctrl+Shift+=` |
| Zoom Out | `Ctrl+Shift+-` |
| Copy Selection | `Ctrl+Shift+C` |
| Paste | `Ctrl+Shift+V` |

**New Tab** splits within the same terminal widget (a tab bar appears at the bottom of the panel).  
**New Terminal Below / Right** spawns a new terminal widget docked below or to the right of the current one. Both inherit the current working directory.

### Close dialog (while "... is still running in this terminal" is up)

| Action | Default |
|--------|---------|
| Close Dialog: Keep Running | `K` |
| Close Dialog: End Session | `E` |
| Close Dialog: Cancel | `Escape` |

These are read only while that dialog is open, which is why single keys are safe —
nothing typed at a shell can reach them. Each button shows its current key, and all
three rebind like any other shortcut.

---

## AI Inventory (when the AI Inventory panel is focused)

| Action | Default |
|--------|---------|
| Focus Filter | `F` |
| Toggle Skills | `S` |
| Toggle Agents | `A` |
| Toggle Commands | `C` |
| Toggle Hooks | `H` |
| Toggle MCP Servers | `M` |
| Toggle Instructions | `I` |
| Jump to a group | `Ctrl` + that group's letter |

Each group's letter is the first letter of its label, underlined in the header. Pressed on
its own it collapses or expands the group; held with `Ctrl` it scrolls the group to the top
of the panel without changing whether it is open. The letters are inert while the filter box
has focus, so typing a filter never collapses anything — press `Esc` to leave the box.
