# Complete Arch Linux i3 + Polybar Cheat Sheet

## i3 Window Manager Keybindings

### Basic Controls
| Keybinding | Action |
|------------|--------|
| `Super + Enter` | Open terminal (Alacritty) |
| `Super + Shift + q` | Close focused window |
| `Super + d` | Open application launcher (Rofi) |
| `Super + Shift + r` | Restart i3 |
| `Super + Shift + c` | Reload configuration |
| `Super + Shift + e` | Exit i3 |
| `Super + Shift + x` | Lock screen |

### Window Management
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

### In Resize Mode
| Keybinding | Action |
|------------|--------|
| `j/Left` | Shrink width |
| `k/Down` | Grow height |
| `l/Up` | Shrink height |
| `;/Right` | Grow width |
| `Enter/Escape/Super+r` | Exit resize mode |

### Workspace Management
| Keybinding | Action |
|------------|--------|
| `Super + 1-0` | Switch to workspace 1-10 |
| `Super + Shift + 1-0` | Move window to workspace 1-10 |

### Media Controls
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
| `Print Screen` | Take screenshot with Flameshot |

## Polybar Modules

### Left Side
| Module | Description | Interaction |
|--------|-------------|-------------|
| **i3** | Workspace indicators | Click to switch workspaces |
| **xwindow** | Current window title | None |

### Center
| Module | Description | Interaction |
|--------|-------------|-------------|
| **date** | Date and time | None |

### Right Side
| Module | Description | Interaction |
|--------|-------------|-------------|
| **filesystem** | Free disk space | None |
| **memory** | RAM usage | None |
| **cpu** | CPU usage | None |
| **temperature** | System temperature | None |
| **pulseaudio** | Volume control | Click to mute, scroll to change volume |
| **brightness** | Screen brightness | None |
| **network** | WiFi status | None |
| **battery** | Battery level/charging | None |
| **powermenu** | System control | Click to open menu |

## Gaps and Appearance
- **Inner gaps**: 15 pixels
- **Outer gaps**: 5 pixels
- **Border width**: 2 pixels
- **Font**: JetBrains Mono 10
- **Smart gaps/borders**: Enabled (only shown when needed)

## Workspaces
| Workspace | Name | Assigned Applications |
|-----------|------|----------------------|
| 1 | Term | Terminal |
| 2 | Web | Firefox |
| 3 | Code | VSCode |
| 4 | Chat | Discord |
| 5 | Media | Spotify |
| 6 | Files | File manager |
| 7 | Gfx | Graphics apps |
| 8 | Misc | Miscellaneous |
| 9 | Misc | Miscellaneous |
| 10 | Sys | System tools |

## Auto-Floating Windows
- Pavucontrol (Volume control)
- Nitrogen (Wallpaper manager)
- Lxappearance (Theme manager)
- Arandr (Display manager)
- Galculator (Calculator)

## Autostart Applications
- Polybar (status bar)
- Picom (compositor for transparency)
- Nitrogen (wallpaper manager)
- nm-applet (network manager)
- volumeicon (volume control)
- dunst (notifications)

## Colors (Nord Theme)

### Window Colors
| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Dark | #2E3440 |
| Alt Background | Dark Gray | #3B4252 |
| Text | Light | #ECEFF4 |
| Alt Text | Light Gray | #D8DEE9 |
| Primary | Blue | #5E81AC |
| Secondary | Light Blue | #8FBCBB |
| Alert | Red | #BF616A |
| Success | Green | #A3BE8C |
| Warning | Yellow | #EBCB8B |
| Purple | Purple | #B48EAD |
| Aqua | Aqua | #88C0D0 |

## Configuration Files
| Component | Path |
|-----------|------|
| i3 config | `~/.config/i3/config` |
| Polybar config | `~/.config/polybar/config.ini` |
| Polybar launch script | `~/.config/polybar/launch.sh` |

## Required Packages
```bash
# Main components
sudo pacman -S i3-gaps polybar picom nitrogen rofi flameshot

# Status bar icons and utilities
sudo pacman -S network-manager-applet volumeicon dunst

# Functionality
sudo pacman -S alacritty playerctl brightnessctl

# Fonts
sudo pacman -S ttf-jetbrains-mono ttf-font-awesome ttf-material-icons noto-fonts-emoji

# Lock screen (AUR)
yay -S betterlockscreen
```

## Commands for System Management
| Command | Action |
|---------|--------|
| `brightnessctl s +10%` | Increase brightness by 10% |
| `brightnessctl s 10%` | Decrease brightness to 10% |
| `pactl set-sink-volume @DEFAULT_SINK@ +5%` | Increase volume by 5% |
| `pactl set-sink-mute @DEFAULT_SINK@ toggle` | Toggle mute |
| `playerctl play-pause` | Play/pause media |
| `playerctl next` | Next track |
| `playerctl previous` | Previous track |
| `betterlockscreen -l blur` | Lock screen with blur |
| `flameshot gui` | Take screenshot with GUI |
| `nitrogen --restore` | Restore wallpaper |

## Troubleshooting
1. **i3 won't start**: Check your config with `i3 -C`
2. **Polybar not showing**: Run `~/.config/polybar/launch.sh` manually to check errors
3. **Icons not displaying**: Ensure fonts are installed correctly
4. **Keybinding not working**: Check for conflicts with `grep "bindsym" ~/.config/i3/config`
5. **Brightness/volume controls not working**: Ensure correct device names in config

## Tips and Tricks
- Use `xprop | grep WM_CLASS` to find window classes for custom rules
- Use `Super+Shift+r` after editing config files to apply changes
- If Polybar fails, i3bar will show as a fallback
- Edit gaps with `gaps inner XX` and `gaps outer XX` in i3 config
- Add custom module scripts to the Polybar config for extended functionality