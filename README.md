# Assignments for Nathan

Choose your favourite programming language and comply as instructed. Don't use any library.


## 1 Dump file as hex


    Sample Command:

        hexdump file1.txt

    Output:


        00000000  89 50 4e 47 0d 0a 1a 0a  00 00 00 0d 49 48 44 52  |.PNG........IHDR|
        00000010  00 00 00 01 00 00 00 01  01 00 00 00 00 37 6e f9  |.............7n.|
        00000020  24 00 00 00 04 67 41 4d  41 00 00 b1 8f 0b fc 61  |$....gAMA......a|
        00000030  05 00 00 00 20 63 48 52  4d 00 00 7a 26 00 00 80  |.... cHRM..z&...|
        00000040  84 00 00 fa 00 00 00 80  e8 00 00 75 30 00 00 ea  |...........u0...|
        00000050  60 00 00 3a 98 00 00 17  70 9c ba 51 3c 00 00 00  |`..:....p..Q<...|
        00000060  02 62 4b 47 44 00 01 dd  8a 13 a4 00 00 00 07 74  |.bKGD..........t|
        00000070  49 4d 45 07 e3 07 1a 08  39 35 87 a4 b0 46 00 00  |IME.....95...F..|
        00000080  00 0a 49 44 41 54 08 d7  63 60 00 00 00 02 00 01  |..IDAT..c`......|
        00000090  e2 21 bc 33 00 00 00 25  74 45 58 74 64 61 74 65  |.!.3...%tEXtdate|
        000000a0  3a 63 72 65 61 74 65 00  32 30 31 39 2d 30 37 2d  |:create.2019-07-|
        000000b0  32 35 54 32 30 3a 35 37  3a 35 33 2b 31 32 3a 30  |25T20:57:53+12:0|
        000000c0  30 ac cd 5d c1 00 00 00  25 74 45 58 74 64 61 74  |0..]....%tEXtdat|
        000000d0  65 3a 6d 6f 64 69 66 79  00 32 30 31 39 2d 30 37  |e:modify.2019-07|
        000000e0  2d 32 35 54 32 30 3a 35  37 3a 35 33 2b 31 32 3a  |-25T20:57:53+12:|
        000000f0  30 30 dd 90 e5 7d 00 00  00 00 49 45 4e 44 ae 42  |00...}....IEND.B|
        00000100  60 82                                             |`.|



## 2 File tree display

    Sample Command:

       tree c:/tmp

    Output:

        dir1
         ├ file1.ext
         ├ file2.ext
         ├ dir1
         │  ├ *file1.ext
         │  ├ ...
         │  └ file2.ext
         ├ dir2
         │  ├ (empty)
         └ eeee.ext
          


## 3a Split files in lines

Sample command:


    split_files myfile.ext 1mb

Output:

    Splitting myfile.ext to 1mb each chunk

    Files:

        myfile.ext.1 (102KB)
        myfile.ext.2 (14KB)
        myfile.ext.3 (5KB)


## 3b Merge

Sample command:


    merge_files  myfile.ext.1  myfile.ext.2  myfile.ext.3 myfile.ext

Output:

    Merging files myfile.ext.1  myfile.ext.2  myfile.ext.3 to myfile.ext ...
    Merging files myfile.ext.1  myfile.ext.2  myfile.ext.3 to myfile.ext ... done.

    Files:

        myfile.ext


## 4 Split files in size

    Sample command:


        split_files myfile.ext 1mb

    Output:

        Splitting myfile.ext to 1mb each chunk

        Files:

            myfile.ext.1 (1024KB)
            myfile.ext.2 (1024KB)
            myfile.ext.3 (512KB)


## 5 Compare text files

    Sample command:

        compare newfile.txt oldfile.txt


    Sample output:

        -- newfile.txt: line 2
        + new line in newfile
        -- newfile.txt: line 6
        - removed line in oldfile
        + replaced line in newfile

    Data:

        newfile.txt:

        the quick
        new line in newfile
        brown fox
        jumps over
        the lazy 
        replaced line in newfile
        grumpy dog

        oldfile.txt:

        the quick
        brown fox
        jumps over
        the lazy 
        removed line in oldfile
        grumpy dog



## 6 CSV Parser

    Sample command:

        read_csv file1.csv


    Sample output:

        ╔═══════════╤═══════════╤═════════════╤═════════════════╗
        ║    col1   │    col2   │    col3     │      col4       ║
        ╠═══════════╪═══════════╪═════════════╪═════════════════╣
        ║ abcd      │ efgh      │ ijkl        │                 ║
        ╟───────────┼───────────┼─────────────┼─────────────────╢
        ║ the quick │ brown fox │ jumps over  │ the lazy dog    ║
        ╟───────────┼───────────┼─────────────┼─────────────────╢
        ║       123 │       456 │             │ 789             ║
        ╚═══════════╧═══════════╧═════════════╧═════════════════╝


## 7 XML Parser

    Sample command:

        parst_xml file1.xml


    Sample output:

        file1.xml
         xml
         ├ tag1
         │  ├ tag2 (attr1="this is attr1 value")
         │  └ tag3
         └ tag2
            ├ tag3
            │  └ "Hello world"
            └ tag3
               └ "another text"


    Data:

        <xml>
            <tag1>
                <tag2 attr1="this is attr1 value"/>
                <tag3><tag3/>
            </tag1>
            <tag2 attr2="tag2 value">
                Hello world
            </tag2>
            <tag3>another text</tag3>
        </xml>



## 8 HTML Parser

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



## 9 GET HTML Texts

Sample command:

    dump_html_text file1.html


Sample output:

    Hello world
    Another text


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


## 10 Socket server (echo)

Sample command:

    echo_server 2345


Sample output:

    telnet localhost 2345
    > hello
    hello



## 11 Socket client

Sample command:

    socket_client localhost 2345


Sample output:

    Connecting to localhost 2345 ... established.
    Sending "hello"
    Server reply "hello"



## 12 Simple Chat P2P

Sample command:

    host:
    chat_p2p myothernickname 2345

    user:
    chat_p2p mynickname other.machine.ip 2345


Sample output:

    host:
        Waiting for client connections at port 2345

        mynickname connected (user ip:port)

        mynickname: Hello
        > Hi there

    user:
        Connecting to other.machine.ip 2345 ...
        Connected as mynickname

        > Hello
        myothernickname: Hi there




## 13 Chat server/client

Sample command:

    server:

        chat_server 2345


    client:

        chat_client localhost 2345



Sample output:

    server:

        Waiting for client connections at port 2345

        Client connected (ip:port)
        Waiting for nickname

        user mynickname connected
        mynickname joing Channel1

        Client connected (ip:port)
        Waiting for nickname

        user myothernickname connected
        myothernickname joing Channel1


    client:

        Connecting server other.machine.ip:2345 ... established.

        Please enter nickname (/nick [nickname])
        > /n
        Bad slash command

        Please enter nickname (/nick [nickname])
        > /nick 
        Name is required

        Please enter nickname (/nick [nickname])
        > /nick admin
        Nickname already taken

        Please enter nickname (/nick [nickname])
        > /nick mynickname
        Your nickname is now mynickname

        Please join a channel (/join [channel])
        > /join
        Channel name is required

        Please join a channel (/join [channel])
        > /join Channel1
        You joined Channel1 (2 users)

        Send message:
        > Hi there!


        myothernickname: Hello mynickname! How are you?




## 14 Proxy server

Sample command:

    proxy 2345 other.machine.ip:4567


Sample output:

    client: GET / HTTP/1.1
    server: **some html text**



## 15 HTTP Server

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



## 16 HTTP Server (Nginx)

Serve static files

Basic Auth



## 17 Secured HTTP Server (Use node js and self-signed certificate)



## 18 SMTP Client

Sample command:


Sample output:


Data:



## 19 POP3 Client

Sample command:


Sample output:


Data:



## 20 FTP Client

Sample command:


Sample output:


Data:



## 21 API Server (via Socket)

Sample command and output:

    Endpoint: /login

    Paramters:

        username: myuser
        password: password123

    Response: OK


    ------------------------------
    Endpoint: /user

    Paramters:


    Response: OK

        userId: user123
        username: myuser
        firstname: myfirstname
        lastname: mylastname



    ------------------------------
    Endpoint: /ceate_user

    Paramters:

        userId: user123
        username: myuser
        password: password123
        firstname: myfirstname
        lastname: mylastname

    Response: OK | NOK [Error text]



## 22 API Server (via HTTP)

Sample command and output (in JSON):

    Endpoint: /login

    Paramters:

        username: myuser
        password: password123

    Response: OK


    ------------------------------
    Get current logged in user

    Endpoint: /user

    Paramters:


    Response:

        userId: user123
        username: myuser
        firstname: myfirstname
        lastname: mylastname



    ------------------------------
    Endpoint: /ceate_user

    Paramters:

        userId: user123
        username: myuser
        password: password123
        firstname: myfirstname
        lastname: mylastname

    Response: OK | NOK [Error text]



    ------------------------------
    Endpoint: /ceate_user

    Paramters:

        userId: user123
        username: myuser
        password: password123
        firstname: myfirstname
        lastname: mylastname

    Response: OK | NOK [Error text]



## 23 Hashing for security (MD5) <- Use "API Server (via HTTP)"



## 24 Web authentications : Basic Auth <- Use "API Server (via HTTP)"




## 25 Web authentications : OAuth 2.0 (with Github)



## 26 Web authentications : SAML 2.0



## 27 Web authentications : Custom login



## 28 Caching : Local



## 29 Caching : Remote (Redis)



## 30 Data Converter : XML to CSV

Sample command:

    convert_xml_to_csv file.xml file.csv


Sample output:
    tag1,tag2,tag3,tag4
    this is tag1,this is tag2,,
    ,Hello world,,
    ,,,another text


Data:
    <xml>
        <RecordSet>
            <Record>
                <tag1>This is tag1</tag1>
                <tag2 attr1="this is attr1 value">this is tag2</tag2>
                <tag3><tag3/>
            </Record>
            <Record attr2="tag2 value">
                <tag2>Hello world</tag2>
            </Record>
            <Record attr2="tag2 value">
                <tag4>another text</tag4>
            </Record>
        </RecordSet>
    </xml>



## 31 Data Converter : File to API

