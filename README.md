# dirwin.py
* Display and 

![N|Solid](/screenshot.png)

dirwin.py is a way to navigate and display window layouts while preserving the z buffer.

# Basic usuage:
- ./dirwin.py list # Show current window layout as ascii
- ./dirwin.py left  # focus window to the left of this one

# Dependencies:
The following binaries must be in your path:
- xprop
- xwininfo
- wmctrl

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