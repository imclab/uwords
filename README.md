uwords
======

Get words from text by grouping together characters from Unicode letter groups
(Lu, Ll, Lt, Lm, Lo).

Installation
------------

    npm isntall uwords

Example
-------

    var uwords = require('uwords');

    var words = uwords('Привет - Hi');

    // words now is [ 'Привет', 'Hi' ]

Details
-------

Returns words from given text by going through the text and grouping together
characters that belongs to one the Unicode Letter groups: Lu, Ll, Lt, Lm, Lo.

Performance
-----------

Run the following command to benchmark the library on your system:

    grunt benchmark

Sample output:

    mb:uwords alex$ grunt benchmark
    Running "benchmark" task
    size=10000000 words=2000000 time=1056ms

Alternatives
------------

The words can be extracted from the text by using the extended regular
expressions library [XRegExp][1]. However, it is 1500x slower.

Run the following command to compare the libraries on your system:

    grunt compare-uwords-xregexp

Sample output:

    mb:uwords alex$ grunt compare-uwords-xregexp --stack
    Running "compare-uwords-xregexp" task
    library=uwords size=1000 words=200 time=2ms
    library=xregexp size=1000 words=200 time=3384ms

You need to install XRegExp to run this comparison.

[1]: http://xregexp.com/