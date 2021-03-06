[![MELPA](https://melpa.org/packages/tango-plus-theme-badge.svg)](https://melpa.org/#/tango-plus-theme)

Tango Plus Theme
================

Color theme for Emacs loosely based on the tango palette.  Like all
themes, this is a work in progress.  The basis for this theme was the
tango theme included in Emacs 24.  Over time colors where added to
increase contrast and support was added for evil, org mode, mu4e,
helm, epresent, markdown, and other modes.

## Installation

Put the file `tango-plus-theme.el` in a directory included in your
load-path.  Add the following line to your start-up file (typically
init.el):

    (load-theme 'tango-plus t)

Alternatively, you can install from
[MELPA](http://melpa.milkbox.net/#/tango-plus-theme).

    (package-install 'tango-plus-theme)

## Screenshots

Note that the colors look more vivid in the screenshots than they are
in Emacs, perhaps that's due to the compression, not sure.

![A search in Evil](Screenshots/screenshot_search.png)
![A Helm session](Screenshots/screenshot_helm.png)

## Design principles

The goal of the theme is to support visual perception and to
facilitate comprehension of code and text.  The goal is not primarily
to look cool.

**Principle 1:** Use colors sparingly.  Give the user subtle hints and
avoid disrupting the reading flow.  For example, coloring LaTeX macros
in red would distract from the text and is therefore considered bad.

**Principle 2:** Use colors as semantic annotation: The meaning of a
color should be largely self-explanatory and consistent across modes.
For instance, red background is used for errors (flyspell) and stuff
that was (ediff) or is going to be deleted (search & replace in evil).
Green background is for matches (isearch) or inserted material
(ediff).  Selections are marked in yellow – think text marker.  All
neutral types of highlights use a light grey for the background
(sentence-highlight-mode, hl-line-mode, show-paren-match).  Foreground
colors: Blue is used for keywords (electric sparks).  Newly defined
stuff like functions and variables are red (hot from the forge).
String and other constants are brown like burned bricks.  Comments are
grey.
