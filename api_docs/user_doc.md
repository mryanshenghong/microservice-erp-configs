*   get current login user for context

    *   /users/user/current GET

    ```
    {
        "code": 200,
        "message": null,
        "data": {
            "id": 1,
            "name": "tester1",
            "email": "tester1@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        }
    }
    ```

*   get user by user_id
    *   /users/user/{user_id} GET


    ```
    {
        "code": 200,
        "message": null,
        "data": {
            "id": 1,
            "name": "tester1",
            "email": "tester1@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        }
    }
    ```

*   get all user list
    *   /users/user?page={0},size={10} GET


    ```
    {
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 1,
            "name": "tester1",
            "email": "tester1@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 2,
            "name": "tester2",
            "email": "tester2@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 3,
            "name": "tester4",
            "email": "tester4@gmail.com",
            "phone": "778899",
            "avatar": null,
            "jobStatus": null
        }
        ]
    }
    ```

*   add a user
    *   /users/user -H Content-Type : application/json POST
    *   name : not null; email : not null; password : not null


    ```
    {
    "name": "tester3",
    "email": "tester11@gmail.com",
    "password" : "111222333",
    "phone": "778899",
    "avatar": "qq_test3.png"
    }
    ```
    ```
    {
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 1,
            "name": "tester1",
            "email": "tester1@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 2,
            "name": "tester2",
            "email": "tester2@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 3,
            "name": "tester4",
            "email": "tester4@gmail.com",
            "phone": "778899",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 6,
            "name": "tester5",
            "email": "tester005@gmail.com",
            "phone": "778899",
            "avatar": "qq_test3.png",
            "jobStatus": "UNDISTRIBUTED"
        }
        ]
    }
    ```

*   update user information

    *   /users/user/{user_id} -H Content-Type : application/json PUT
    *   name: not null; email: not null; password: not null

    ```
    {
    "name": "tester4",
    "email": "tester4@gmail.com",
    "password" : "111222333",
    "phone": "778899",
    "avatar": "qq_test3.png"
    }
    ```

    ```
    {
    "code": 200,
    "message": null,
    "data": {
        "id": 3,
        "name": "tester4",
        "email": "tester4@gmail.com",
        "phone": "778899",
        "avatar": null,
        "jobStatus": null
        }
    }
    ```

*   delete user

    *   /users/user/{user_id} DELETE

    ```
    {
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 1,
            "name": "tester1",
            "email": "tester1@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 2,
            "name": "tester2",
            "email": "tester2@gmail.com",
            "phone": "1122334455",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 3,
            "name": "tester4",
            "email": "tester4@gmail.com",
            "phone": "778899",
            "avatar": null,
            "jobStatus": null
        },
        {
            "id": 6,
            "name": "tester5",
            "email": "tester005@gmail.com",
            "phone": "778899",
            "avatar": "qq_test3.png",
            "jobStatus": "UNDISTRIBUTED"
        }
        ]
    }
    ```

* get user direct permissions
    * /users/user/{user_id}/permissions
    ```
    {
    "code": 200,
    "message": null,
    "data": {
        "admin": {
            "create": false,
            "update": false,
            "read": false,
            "delete": false
        },
        "inventory": {
            "create": false,
            "update": false,
            "read": false,
            "delete": false
        },
        "user": {
            "create": true,
            "update": true,
            "read": true,
            "delete": true
        }
        }
    }
    ```
