# Apple keyboard for linux console

For macbook pro: 
put ru-apple-mbp.map.gz to foldel with keymaps (like /usr/lib/kbd/keymaps/legacy/mac/all/.)

in /etc/vconsole.conf set ``KEYMAP="ru-apple-mbp"`` 

.tmux.conf example:
```
bind -N "Turn display backlight up"    -n S-F1  run-shell "brightnessctl -q s 5%-"
bind -N "Turn display backlight down"  -n S-F2  run-shell "brightnessctl -q s 5%+"

bind -N "Turn keyboard backlight up"   -n S-F5  run-shell "brightnessctl -q --device='kbd_backlight' s 5%-"
bind -N "Turn keyboard backlight down" -n S-F6  run-shell "brightnessctl -q --device='kbd_backlight' s 5%+"

bind -N "Toggle volume"    -n S-F10 run-shell 'amixer -q sset Master toggle'
bind -N "Turn up volume"   -n S-F11 run-shell 'amixer -q sset Master 3%-'
bind -N "Turn down volume" -n S-F12 run-shell 'amixer -q sset Master 3%+'
```
