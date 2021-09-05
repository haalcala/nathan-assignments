# 22 API Server (via HTTP)

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
