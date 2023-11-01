# FIND-PAN

[![Build Status](https://travis-ci.org/adamcaudill/find-pan.svg?branch=master)](https://travis-ci.org/adamcaudill/ccsrch)

FIND-PAN is a linux for searching filesystems for credit card information, based on Adam Caudill's fork of Mike Beekey's ccsrch. I've renamed, updated the prefix rules and tweaked & tidied-up for NPP's Linux-only needs.

This program is free software; you can redistribute it and/or modify it under  the terms of the GNU General Public License as published by the Free  Software Foundation; either version 2 of the License, or (at your option)  any later version.

### Using FIND-PAN

```
Usage: ./find-pan <options> <start path>
  where <options> are:
    -a             Limit to ASCII files.
    -b             Add the byte offset into the file of the number
    -e             Include the Modify Access and Create times in terms
                   of seconds since the epoch
    -f             Just output the filename with potential PAN data
    -i <filename>  Ignore credit card numbers in this list (test cards)
    -j             Include the Modify Access and Create times in terms
                   of normal date/time
    -o <filename>  Output the data to the file <filename> vs. standard out
    -t <1 or 2>    Check if the pattern follows either a Track 1
                   or 2 format
    -T             Check for both Track 1 and Track 2 patterns
    -c             Show a count of hits per file (only when using -o)
    -s             Show live status information (only when using -o)
    -l N           Limits the number of results from a single file before going
                   on to the next file.
    -n <list>      File extensions to exclude (e.g., .json,.tc)
    -m             Toggle PAN number masking (now ON by default).
    -w             Check for card matches wrapped across lines.
    -x             Don't display file stat errors (not found, etc.)
    -v             Be a bit more verbose in some instances

    -h             Usage information
```

Updated Source for Credit Card Prefixes:  
https://en.wikipedia.org/wiki/Payment_card_number#Issuer_identification_number_(IIN)

Updated to look for Visa, Mastercard, American Express, Discover, JCB, UnionPay, & Diners Club only
Mask PANs by default
Allow for comment lines (start with #) in ignore files

### Building
```
$ git clone https://github.com/SG185369/find-pan.git
$ cd find-pan
$ mkdir build
$ cd build
$ cmake ..
$ make
```
