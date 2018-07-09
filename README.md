```
Usage:
recorddesktop [FFOPT] [OPT] [+PRESET] [REGION] FILE
Record desktop REGION to FILE, using ffmpeg with x11grab

REGION can be specified as:
  WxH+X+Y       Record Width * Height region, positioned at X, Y

  screen[N]     Record X screenN, where N defaults to 0.
                Gets screen dimensions from xrandr.
                This typically captures the entire desktop.

  rect          Select a rectangular region to record
                Requires xrectsel.

  WxH           Select a rectangular region, but scale
                selection to WxH. Requires xrectsel.

  W:H           Select a rectangular region, but grow
                selection to W:H aspect ratio. Requires xrectsel.

  win           Select a X11 client window to record.
                Requires xwininfo, xdotool or wmctrl.

  Not specifying a region captures the entire desktop.

FFOPT are options passed to ffmpeg
  Single-dash options (-option) are passed to ffmpeg

PRESET is a named set of ffmpeg options, which may be extended
or overridden in ~/.recorddesktop. Presets are declared as:

[name] [ffmpeg options]+

and then applied on the command line as +name. Multiple presets
may be applied.

Options:

  --dry-run    Print command and exit only, do not run ffmpeg
  --presets    List defined presets and exit
  --help       Display this help text and exit
```
