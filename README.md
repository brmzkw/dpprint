dpprint - date prefixed print
=============================

Read lines on stdin and prefix each of them with the current date.

To avoid buffering, use *stdbuf(1)*.

Example:

    stdbuf -o0 long_command | dpprint

Note that dpprint is relatively useless, as it is a very simple wrapper on
*gawk(1)*.
