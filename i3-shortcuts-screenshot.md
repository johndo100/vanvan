# i3 screenshot shortcuts

## Requirements
- [maim](https://github.com/naelstrof/maim)
- [xclip](https://github.com/astrand/xclip)
- [xdotool](https://github.com/jordansissel/xdotool)

## Set-up

Set this on your i3 config file `~/.i3/config`

Read more from [i3 User’s Guide](https://i3wm.org/docs/userguide.html#_using_i3).

```
## Screenshots
bindsym Print exec --no-startup-id maim ~/Pictures/screenshots/$(date +%y-%m-%d--%H-%M-%S_maim | tr A-Z a-z).jpg
bindsym $mod+Print exec --no-startup-id maim --window $(xdotool getactivewindow) ~/Pictures/screenshots/$(date +%y-%m-%d--%H-%M-%S_maim | tr A-Z a-z).jpg
bindsym Shift+Print exec --no-startup-id maim --select ~/Pictures/screenshots/$(date +%y-%m-%d--%H-%M-%S_maim | tr A-Z a-z).jpg

## Clipboard Screenshots
bindsym Ctrl+Print exec --no-startup-id maim | xclip -selection clipboard -t image/png
bindsym Ctrl+$mod+Print exec --no-startup-id maim --window $(xdotool getactivewindow) | xclip -selection clipboard -t image/png
bindsym Ctrl+Shift+Print exec --no-startup-id maim --select | xclip -selection clipboard -t image/png
```

> You may remove the default screenshot shortcuts to prevent error

## What it does

| Feature | Shortcut |
| :----- | :------ |
| Full Screen | `PrtScrn` |
| Selection | `Shift` + `PrtScrn` |
| Active Window | `Super` + `PrtScrn` |
| Clipboard Full Screen | `Ctrl` + `PrtScrn` |
| Clipboard Selection | `Ctrl` + `Shift` + `PrtScrn` |
| Clipboard Active Window | `Ctrl` + `Super` + `PrtScrn` |

> All the screen shots are saved on `~/Pictures/screenshots` in jpg format. 

> `super` key is the _windows_ key

Original [here](https://gist.github.com/dianjuar/ee774561a8bc02b077989bc17424a19f)

[@dianjuar](https://github.com/dianjuar)
