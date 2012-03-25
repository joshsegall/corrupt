corrupt
=======

Command line utility to simulate file corruption.

Given an input file it randomly corrupts bits or characters, which can be useful in testing how well other programs deal with file corruption. Options include setting the bit error rate, truncating files, adding garbage to the end of files, and running on ascii and binary files.

Dependencies
------------

Python 2.6+

Usage
-----

Corrupt approximately every 100,000th bit (bit error rate of 10e-5):

    python corrupt.py -n 100000 infile -o outfile

Corrupt, and also truncate after 4K:

    python corrupt.py -t 4096 infile -o outfile

Corrupt, and add 30 bytes of random data at the end

    python corrupt.py -g 30 infile -o outfile

Corrupt a text file, ensuring output is printable ASCII characters:

    python corrupt.py -a input.txt -o output.txt

Input/output defaults to stdin/stdout if no files specified

    python corrupt.py < infile > outfile

All the above options can be combined.

