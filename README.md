dpprint - date prefixed print
=============================

Read lines on stdin and prefix each of them with the current date.

To avoid buffering, use *stdbuf(1)*.

Example:

    stdbuf -o0 long_command | dpprint

Note that dpprint is relatively useless, as it is a very simple wrapper on
*gawk(1)*.


Example
-------

    # for x in $(seq 5); do echo $x; sleep 1; done | dpprint
    [2014-11-26 14:21:21] 1
    [2014-11-26 14:21:22] 2
    [2014-11-26 14:21:23] 3
    [2014-11-26 14:21:24] 4
    [2014-11-26 14:21:25] 5

Build
-----

To build the debian package, run:

    debuild -us -uc
