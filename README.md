# bin2ihex
Converts a binary to and from a subset of [Intel-format HEX file](https://en.wikipedia.org/wiki/Intel_HEX).

~~~~
Usage:
-b:              Forces binary-to-hex.
-x:              Forces hex-to-binary.
-o:              Sets the output filename.
                 (Default: input with new extension)
-s:              Sets the data size per line. (for bin->hex)
                 (Between 1 and 255. Default: 1 byte.)
-h or --help:    Gives you this text.
-v or --version: Prints the version.
~~~~

Made for use with Quartus II, which (at least in the version I need to use) only supports two file-formats for initializing memory and doesn't let me just load a binary. Hopefully this can be useful for other use cases.

Because of my simple use case, I only need to support the "Data" and "End Of File" record types. I also don't really care about any data size besides "1" even though I support it for both conversions, so I haven't tested it with any program that needs it, like flashing a microcontroller.

Tested on both Windows and macOS.