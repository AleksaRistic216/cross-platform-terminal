# Customization

## Keyboard Shortcuts

### In-app rebinding

Open **CPT logo → Settings → Global Shortcuts**. Each action shows its current binding; click **Rebind** to capture a new key combo. Use **Reset** to restore a single action's default, or **Reset All** to restore all defaults.

### Config file

Shortcuts are persisted to:

```
~/.config/cpt/shortcuts.json
```

The file is written automatically when you save changes in the UI. You can also edit it by hand — the app loads it on startup.

**Format:**

```json
{
  "resolution_mode": "widget_overrides_global",
  "bindings": [
    {
      "action_id": "terminal.new_tab",
      "scope": "Terminal",
      "keycode": 116,
      "ctrl": true,
      "shift": true,
      "alt": false
    }
  ]
}
```

- `action_id` — internal action name (e.g. `view.new`, `terminal.zoom_in`)
- `scope` — `"global"` for workspace-wide shortcuts, `"Terminal"` for terminal-only
- `keycode` — SDL3 keycode integer
- `ctrl` / `shift` / `alt` — modifier flags

Only bindings that differ from the defaults need to be listed; omitted actions keep their defaults.

### Resolution mode

When a global shortcut and a terminal-scoped shortcut share the same key combo, `resolution_mode` decides which wins:

| Value | Behavior |
|-------|----------|
| `widget_overrides_global` | Terminal shortcuts take priority when a terminal is focused (default) |
| `global_overrides_widget` | Global shortcuts always fire, even inside a terminal |

---

## Config Directory

All persistent state lives in the platform config directory:

| Platform | Path |
|----------|------|
| Linux | `~/.config/cpt/` |
| Windows | `%APPDATA%\cpt\` |

| File | Contents |
|------|----------|
| `shortcuts.json` | Custom key bindings |
| `workflows.json` | Saved workflows |
| `layout.json` | View and widget layout, restored on next launch |

Delete any of these files to reset that aspect of the app to defaults.
