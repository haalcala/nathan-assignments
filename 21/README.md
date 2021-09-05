# 21 API Server (via Socket)

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
