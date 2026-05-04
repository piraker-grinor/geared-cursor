# geared-cursor
Geared is a pre-rendered 3D animated cursor for Linux.
Complete set of 32x animated cursors made for Xfce desktop, not sure about others but they will probably work too.
This cursor is likely better suited for light themes, but is still perfectly usable on dark themes.

Colour palette from Fallout 2.
All assets are created by me or licensed under CC0.
## Installation
Download and extract the [latest release](https://github.com/piraker-grinor/geared-cursor) to ``~/.local/share/icons/`` and set your cursor theme to Geared.
## Rendering
Provided is information related to rendering the cursor for whatever reason. You will need [Blender](https://blender.org) and [ImageMagick](https://imagemagick.org)

Upon opening one of the ``.blend`` files, the texture of the dark grey material might be missing because I'm lazy, simply set the images in the material to the ones provided in ``/Metal027``. Variants of the cursors (such as "not-allowed" or "copy") can be made by un-hiding one of the hidden unorganised objects. For most of the animations they are 32 frames each, except for the hand's grab animation (available in the actions tab), which is 16 frames, which should be set on the timeline before rendering. You can then render the animation to a folder in ``/render`` (such as ``/default`` or ``/hand``) and run the following ImageMagick command within that folder:
```
magick *.png -channel A -threshold 20% -channel RGB -dither FloydSteinberg -remap ../fallout.png output%04d.png
```
The output frames can then be used to assemble an X11 cursor.
All frames should be 2/60ths of a second, and the hot spots for each cursor are as follows:
- "wait" cursor: ``{13,13}``
- hand cursors: ``{16,13}``
- arrow, zoom and text cursors: ``{15,15}``
- everything else: ``{0,0}``
