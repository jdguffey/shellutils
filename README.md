# shellutils

This repo contains various shell (POSIX or otherwise) utilities, divided by directory into a few subprojects.

I could actually create separate repos for each and add them "the right way" as git submodules, but I really don't feel like it right now.

## Subprojects

cp-progress:
    This subdirectory contains a simple implementation of cp(1) with a progress bar. If it is passed any flags it doesn't understand (anything except -r), the script will pass everything to the system implementation of the utility.

userspace-emul:
   This subdirectory contains (or will by the time I'm done implementing things) most of the GNU utilities in script form. The goal is to provide a portable implementation of the GNU userspace for systems that don't have it (\*BSD, Solaris, busybox, et al). If GNU utilities already exist, the scripts will pass all input to them. At this time, if any implementation of a utility already exists, the scripts will pass all input to them, though in the future I expect to implement wrapping functionality (consider FreeBSD sed's -E vs. GNU sed's -r).

## Installation

At this time, installation is handled by prepending the cp-progress and/or userspace-emul directories to your $PATH, as such:

(in ~/.bashrc or similar):
export "PATH=~/bin/shellutils/cp-progress:~/bin/shellutils/userspace-emul:$PATH"

Someday I plan to also implement an installation script that may do something slightly more intelligent.

## Disclaimer

This is a project I'm working on in my downtime and is likely to be buggy, incomplete, and what have you. Use it at your own risk, YMMV, etc. I'm not responsible if you trash your production boxes, summon Cthulu, or are inconvenienced by this code.

