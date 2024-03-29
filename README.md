# dirwin.py
dirwin.py is a way to navigate windows quickly with the keyboard by relative direction, while preserving the z buffer.


![N|Solid](/screenshot.png)


https://user-images.githubusercontent.com/13475516/133817234-d7ac8ed0-81c4-4d4e-b975-670c21aa315b.mp4



# Basic usuage:
- ./dirwin.py list # Show current window layout as ascii
- ./dirwin.py left  # focus window to the left of this one

# Requires:

- xprop: window stack order and desktop geometry
- xdotool: identify selected window and move mouse
- xwininfo: window geometry information
- wmctrl: change focus

# Directional movement:
- Directional movement is a pretty useful feature in dynamic and tiling window managers, if like me you still prefer WM's like Openbox this script is a way to get that functionality.

Map it in openbox:

    <keybind key="W-Left">
      <action name="Execute">
        <command>~/scripts/dirwin.py left</command>
      </action>
    </keybind>

    
    <keybind key="W-Right">
      <action name="Execute">
        <command>~/scripts/dirwin.py right</command>
      </action>
    </keybind>

    
    <keybind key="W-Up">
      <action name="Execute">
        <command>~/scripts/dirwin.py up</command>
      </action>
    </keybind>

    
    <keybind key="W-Down">
      <action name="Execute">
        <command>~/scripts/dirwin.py down</command>
      </action>
    </keybind>

    
# Configuration:
You can set scale to a lower value for speed (1 for a real-sized screen buffer), but this will start negatively improving accuracy at around 32.

# TODO:
* Improve accuracy
* Better filtering for panels
