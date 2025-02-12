---
title: LIQUIDSOAP
section: 1
date: Jul 24, 2019
header: Liquidsoap 1.4.0
footer: Liquidsoap 1.4.0
...

<!-- .TH LIQUIDSOAP 1 "Jul 1, 2016" "Liquidsoap 1.4.0" -->

# NAME

liquidsoap - a multimedia streaming language

# SYNOPSIS
liquidsoap [ _options_ ] [ _script_ | _expression_ ]

# DESCRIPTION

Liquidsoap is a programming language for describing multimedia streaming systems.
It is very flexible, making simple things simple but giving a lot
of control for advanced uses. Liquidsoap
supports audio, video and MIDI streams,
and a wide range of input/output operators
including Icecast and various soundcard APIs.
It can perform a broad range of signal processing,
combine streams in various ways, support custom transitions,
generate sound procedurally...
and all this can be assembled as you wish.
Input files can be accessed remotely, or even be synthesized on the fly
using external scripts such as speech synthesis.
Finally, interaction with a running liquidsoap instance is possible
via telnet or socket.

Liquidsoap scripts passed on the command line will be evaluated: they shall be
used to define the streaming system to be ran.  It is possible to pass multiple
scripts; they will all be ran successively, and definitions from one script can
be used in subsequent ones.  A script will be read from standard input if `-` is
given as script filename.  Information about scripting liquidsoap is available
on our website: [http://liquidsoap.info/](http://liquidsoap.info/).

If the parameter is not a file it will be treated as an expression which will
be executed. It is a convenient way to test simple one-line scripts. When
running only one-liners, the default is to log messages directly on stdout
rather than to a file.

# OPTIONS

\-
: Read script from standard input.

\--
: Stop parsing the command-line and pass subsequent items to the
script.

\--debug
: Print debugging log messages.

\--dynamic-plugins-dir _path_
: Directory where to look for plugins.


\--errors-as-warnings
: Issue warnings instead of fatal errors for unused variables and ignored
  expressions. If you are not sure about it, it is better to not use it.

\--interactive
: Start an interactive interpreter.

\--list-plugins
: List all plugins (builtin scripting values, supported formats and protocols).

\--list-plugins-xml
: List all plugins (builtin scripting values, supported formats and protocols), output as XML.

\--no-pervasives
: Do not load pervasive script libraries.

\--version
: Display Liquidsoap's version.

-c, \--check
: Check and evaluate scripts but do not perform any streaming.

-cl, \--check-lib
: Like \--check but treats all scripts and expressions as libraries, so that
  unused toplevel variables are not reported.

-d, \--daemon
: Run in daemon mode.

-f, \--force-start
: For advanced dynamic uses: force liquidsoap to start even when no active
  source is initially defined.

-h _plugin_
: Print the description of a plugin, eg. a builtin scripting function.

-i
: Display inferred types.

-p, --parse-only
: Parse scripts but do not type-check and run them.

-q, \--quiet
: Do not print log messages on standard output.

-r _filename_
: Process a request.

-T, \--disable-telnet
: Disable the telnet server.

-U, \--disable-unix-socket
: Disable the unix socket.

-t, \--enable-telnet
: Enable the telnet server.

-u, \--enable-unix-socket
: Enable the unix socket.

-v, \--verbose
: Print log messages on standard output.

\--conf-descr-key _key_
: Describe a configuration key.

\--conf-descr
: Show all configuration keys with their documentation.

\--conf-descr-liqi
: Show all configuration keys with their documentation in liqi (documentation wiki) format.

\--conf-dump
: Dump the configuration state

-help, \--help
Display this list of options

# SEE ALSO

Our website [http://liquidsoap.info/](http://liquidsoap.info/) and the HTML
documentation coming with your distribution of Liquidsoap.

# AUTHOR

[The savonet team](savonet-users@lists.sourceforge.net).
