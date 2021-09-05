# 13 Chat server/client

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
