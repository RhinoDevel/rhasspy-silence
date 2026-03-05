To-do after installation and Python setup
-----------------------------------------
(Marcel Timm, RhinoDevel, 2026mar05)

At least in Debian 13, with Python 3.13, webrtcvad won't work, because
pkg_resources cannot be found (I don't know why).

The webrtcvad file should have been installed at

MtLlmWinCis/client/venv/lib/python3.13/site-packages/webrtcvad.py

You need to comment out the line

import pkg_resources

and replace the line

__version__ = pkg_resources.get_distribution('webrtcvad').version

with something like

__version__ = "MT-Hack-Version"

to make it run.

Maybe there is a smarter solution to this..!
