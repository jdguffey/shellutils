### userspace-emul ###

This collection of utilities provides a GNU-like userspace wrapper for whatever userland utilities happen to already be installed.

## Options ##

These scripts attempt to replicate GNU's option support as much as possible. Currently only options appearing *before* required parameters (file names, etc.) are supported.

## Usage ##

To use these scripts, place them in your PATH. For example, if you are using bash and have this repository cloned in ~/, add:

    PATH="~/shellutils/userspace-emul:$PATH"

to ~/.bashrc or ~/.bash\_profile as necessary, reload your shell (or execute "source ~/.bashrc") and use any scripts here as normal commands.

As much as possible, scripts provided here attempt to provide the same userspace experience (more or less) that GNU does. For instance, if you're on FreeBSD and want to use stat(1) to see how many bytes a file has, execute "stat -c %b," using the stat script contained here rather than concerning yourself with the fact that FreeBSD's command to do the same is "stat -f %z."

