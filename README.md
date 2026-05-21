# geared-cursor
Geared is a pre-rendered 3D animated cursor for Linux.
Complete set of 32x and 64x animated cursors made for Xfce desktop, not sure about others but they will probably work too.
This cursor is likely better suited for light themes, but is still perfectly usable on dark themes.

Colour palette from Fallout 2.
All assets are created by me.
## Installation
Download and extract the [latest release](https://github.com/piraker-grinor/geared-cursor) to ``~/.local/share/icons/`` and set your cursor theme to Geared.
## Rendering
### Prerequisites
- [Blender](https://blender.org)
- [ImageMagick](https://imagemagick.org)
- xcursorgen

The project has been overhauled entirely to render, quantise, and generate the cursors automatically.
All materials are stored in the ``default.blend`` file, where they are linked to the other blend files automatically.
You can then change the materials to your preferred colour.
You can set the desired resolution in the Output tab on the right.

To render, go to the Scripting workspace at the top and click on the 'Run Script' button.
This will automatically render each cursor variant, and may take a while; wait until the run button has turned back to grey.
This process must be repeated for each ``.blend`` file.

The outputted cursors will be stored in ``render/final/`` where you can then copy-paste into the cursor theme folder.
