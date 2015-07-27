### cp-progress ###

This utility provides a cp(1)-like function that shows a progress bar as things are copied.

## Options ##

This script only makes use of the -r flag. If any other flags are passed, then all parameters are passed to cp(1) and no progress bar is displayed, to ensure that system functionality is never lost.

## Usage ##

If this script is called with no flags, it copies a single file from src (parm1) to dst (parm2) through a pipe and displays a progress bar to show status.

If this script is called with the -r flag, it <something> and displays a progress bar to show status.

If this script is called with any unknown flag, it passes all arguments to the system's cp(1) utility.

