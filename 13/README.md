# 12 Simple Chat P2P

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
