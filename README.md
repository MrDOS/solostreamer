# solostreamer

Fetching output of the [RBRsolo T][0]
is unlike that of other more modern
RBR instruments.
Notably,
fetches output raw, uncalibrated A/D measurements
instead of engineering units,
do not output sub-second timestamps,
and columns of output
are not comma-separated.
solostreamer continuously fetches
from a solo T
and amends these issues
and produces output much like that
of the [RBRcoda T][1].

Because the water- and pressure-proof housing
of the instrument
must be opened
in order to access the USB port,
this script is pretty much only useful
for logging in air.
Which is fine,
because that's what I wanted to do.
YMMV.

[0]: https://rbr-global.com/products/compact-loggers/rbrsolo-t
[1]: https://rbr-global.com/products/sensors

## Installation

It's a script. Download it, run it.

It requires Python 3, [pySerial][2], and [regex][3].

[2]: https://pypi.python.org/pypi/pyserial
[3]: https://pypi.python.org/pypi/regex

## Usage

    $ ./solostreamer /dev/tty.usbmodem 1421

That's it.

The script is unforgiving
and will simply vomit and die
if you do not invoke it
as it expects to be run.

## Disclaimer

At time of writing,
I work for [RBR][4].
This script was developed
on my own time
and does not constitute
an official RBR product,
nor is it supported by RBR
in any fashion.
Neither RBR nor myself are to be held liable
if this script causes your computer or your solo
to flood,
catch fire,
vanish into another dimension,
or misbehave in any other way.
I'm making it public
as much because GitHub is an integral part of my backup scheme
as because I hope it can be useful to someone else.

[4]: http://rbr-global.com/
