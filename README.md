# tblib

A Trackback (client) implementation in Python

    >>> import tblib
    >>> tb = tblib.TrackBack()
    >>> tb.autodiscover('http://Queue/weblog/matt/archives/2003_01.html#000007')
    >>> print tb.tbUrl
    http://Queue/weblog/mt-tb.cgi/7
    >>> tb.blog_name = 'My Weblog'
    >>> tb.title = 'This Post Will Ping That Weblog Entry'
    >>> tb.url = 'http://postneo.com'
    >>> tb.excerpt = 'I released tblib 0.1.0 today.  It supports autodiscovery...'
    >>> tb.ping()
    >>> print tb.tbErrorCode
    0

## Command Line Interface

    $ tbclient.py -tburl http://Queue/weblog/mt-tb.cgi/7 -title "My Title" -excerpt "My Excerpt" -url http://postneo.com -blogname "My Weblog Name"
    Trackback command line client here.  Preparing TrackBack...
    TrackBack URL: http://Queue/weblog/mt-tb.cgi/7
    TrackBack Title: My Title
    TrackBack Excerpt: My Excerpt
    Your URL: http://postneo.com
    Your Weblog Name: My Weblog Name
    Pinging http://Queue/weblog/mt-tb.cgi/7...
    HTTP Response: 200 OK
    TrackBack Error Code is: 0 (zero is okay)
    Done!

## License

Copyright 2003, Matt Croydon

Licensed under GPL.
