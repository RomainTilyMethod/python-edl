python-edl
==========

A python EDL (Edit Decision List) parsing library, based on the ruby EDL
library by Julik Tarkhanov http://guerilla-di.org/edl/. Still a work in
progress so collaboration welcome.

Uses pytimecode.py to handle the Timecode mathematics.
<br>Merge master with MiguelUpdate that contained fixes.<br>

Forked and tested on <b>Python3.11</b>

https://github.com/simonh10/python-edl

Usage::

    from edl import Parser
    parser=Parser('23.98')
    with open('file.edl') as f:
        edl=parser.parse(f)
        for event in edl.events:
            print "Event Number:"+str(event.num)
            print "Source file:"+str(event.source_file)
            print "Clip Name:"+str(event.clip_name)

Accepted framerate values ['60', '59.94', '50', '30', '29.97', '25', '24',
'23.98'] whole number frame rates are more tested than others, but the accuracy
relies heavily on accuracy of the pytimecode library.

Documentation for pytimecode can be found
[here](https://code.google.com/p/pytimecode/).

(The MIT License)

Copyright © 2013 Simon Hargreaves <simon@simon-hargreaves.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the ‘Software’), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
