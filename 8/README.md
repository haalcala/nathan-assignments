# 8 HTML Parser

Sample command:

    parst_html file1.html

Sample output:

    file1.html
     html
     ├ head
     │  ├ link (rel=)
     │  └ meta
     └ body
        ├ div
        │  ├ "Hello"
        │  ├ br
        │  └ "world"
        └ "another text"

Data:

    <html>
        <head>
            <title>This is the title
            </title>
        </head>
        <body>
            Hello<br/>world
        </body>
    </html>
