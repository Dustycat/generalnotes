
https://www.joeysretrohandhelds.com/guides/apollo-artemis-streaming-setup-guide/

# Resolutions

## Option 1
Moonlight: Set to Native Resolution: 2736x1824
ASUS Apollo: Set to half resolution 1368x912

## Option 2
Moonlight: Set to Native Resolution: 1368x912

Note: With this setup, I can't change the ASUS Apollo resolution

# Moving App that is outside the Main Window

If your App is outside of Main Window

1. Go to task bar and right click app
2. Select move, then use arrow key. If it's on window 1, then use the right arrow

# Setup Virtual Display

Applications: Desktop

1. Make sure Always use Virtual Display: Checked. This just means virtual display is enabled
2. General:Configuration, add the following. Option 4 is to extend desktop to virtual display. Option 3 switches to the second display (or virtual monitor) _only_.
	1. DO: displayswitch.exe 4
	2. UNDO: displayswitch.exe 3

Summary Table for Apollo/Sunshine Setup

|Command|Windows Switch|Typical Use|
|---|---|---|
|`displayswitch.exe 1`|/internal|Re-enables your main physical monitor (used on stream end).|
|`displayswitch.exe 3`|/extend|Extends desktop to virtual/second screen.|
|`displayswitch.exe 4`|/external|**Best fo**|
3. Under General:Configuration, configure so that all apps on the virtual
	1. Check `Headless Mode`