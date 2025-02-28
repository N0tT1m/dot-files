# i3 Window Manager Cheat Sheet

## Basic Controls
| Keybinding | Action |
|------------|--------|
| `Super + Enter` | Open terminal (Alacritty) |
| `Super + Shift + q` | Close focused window |
| `Super + d` | Open application launcher (Rofi) |
| `Super + Shift + r` | Restart i3 |
| `Super + Shift + c` | Reload configuration |
| `Super + Shift + e` | Exit i3 |

## Window Management
| Keybinding | Action |
|------------|--------|
| `Super + j/k/l/;` | Change focus (left/down/up/right) |
| `Super + Arrow Keys` | Change focus (left/down/up/right) |
| `Super + Shift + j/k/l/;` | Move window (left/down/up/right) |
| `Super + Shift + Arrow Keys` | Move window (left/down/up/right) |
| `Super + h` | Split horizontally |
| `Super + v` | Split vertically |
| `Super + f` | Toggle fullscreen |
| `Super + s` | Stacking layout |
| `Super + w` | Tabbed layout |
| `Super + e` | Toggle split layout |
| `Super + Shift + Space` | Toggle floating mode |
| `Super + Space` | Toggle focus between tiling/floating |
| `Super + a` | Focus parent container |
| `Super + r` | Enter resize mode |
| `Super + Mouse` | Drag floating windows |

## Workspace Management
| Keybinding | Action |
|------------|--------|
| `Super + 1-0` | Switch to workspace 1-10 |
| `Super + Shift + 1-0` | Move window to workspace 1-10 |

## Workspace Names
| Workspace | Name |
|-----------|------|
| 1 | Home/Terminal |
| 2 | Web Browser |
| 3 | Code Editor |
| 4 | Chat/Discord |
| 5 | Music/Spotify |
| 6 | File Manager |
| 7 | Graphics |
| 8 | Misc |
| 9 | Misc |
| 10 | System |

## Media Controls
| Keybinding | Action |
|------------|--------|
| `Volume Up Key` | Increase volume by 5% |
| `Volume Down Key` | Decrease volume by 5% |
| `Mute Key` | Toggle mute |
| `Brightness Up Key` | Increase brightness by 10% |
| `Brightness Down Key` | Decrease brightness by 10% |
| `Play/Pause Media Key` | Play/Pause media |
| `Next Media Key` | Next track |
| `Previous Media Key` | Previous track |

## Special Functions
| Keybinding | Action |
|------------|--------|
| `Super + l` | Lock screen |
| `Print Screen` | Take screenshot with Flameshot |

## Gaps Control (i3-gaps)
- Inner gaps: 15 pixels
- Outer gaps: 5 pixels
- Smart gaps/borders: enabled (only shown when needed)

## Autostart Applications
- Polybar: Custom status bar
- Picom: Window compositor for transparency
- Nitrogen: Wallpaper manager
- nm-applet: Network manager
- volumeicon: Volume control applet
- dunst: Notification daemon

## Colors (Nord Theme)
- Active window: Blue (#5E81AC)
- Inactive window: Dark gray (#3B4252)
- Urgent window: Red (#BF616A)

## Floating Windows (Automatic)
- Pavucontrol (Volume control)
- Nitrogen (Wallpaper manager)
- Lxappearance (Theme manager)
- Arandr (Display manager)
- Galculator (Calculator)

## Workspace Assignments
- Firefox → Workspace 2
- VSCode → Workspace 3
- Discord → Workspace 4
- Spotify → Workspace 5

## Configuration File Location
`~/.config/i3/config`