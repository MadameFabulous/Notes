```
# Start tmux sessions with an index of 1
set -g base-index 1
set -g renumber-windows on

# Set the status bar at the top
set-option -g status-position top

# Set the status bar background color to color55 and text color to white
set-option -g status-bg color55
set-option -g status-fg white

# Customize the left and right status
set-option -g status-left " ⚧️ "
set-option -g status-right "#(ip -4 addr show tun0 | awk '/inet / {print $2}' | cut -d/ -f1)|#(ip -4 addr show eth0 | awk '/inet / {print $2}' | cut -d/ -f1)"

#mouse mode
bind m set -g mouse on
bind M set -g mouse off
```
