# 15 HTTP Server

Sample command:

    http_server 80

Sample output:

    Listening for http connections at port 80:



    C:> Telnet localhost 80
    GET / HTTP/1.1<enter>
    <enter>

    <html>
        <head>
            <title>This is the title
            </title>
        </head>
        <body>
            Hello<br/>world
        </body>
    </html>
