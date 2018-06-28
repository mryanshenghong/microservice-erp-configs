* get current login user for context
    * /users/user/current     GET
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


* get user by user_id
    * /users/user/{user_id}       GET
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

* get all user list
    * /users/user?page={0},size={10}       GET
    ```
    {
        "code": 200,
        "message": null,
        "data": {
            "content": [
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
                    "name": "tester3",
                    "email": "tester3@gmail.com",
                    "phone": "1122334455",
                    "avatar": null,
                    "jobStatus": null
                }
            ],
            "last": true,
            "totalPages": 1,
            "totalElements": 3,
            "size": 10,
            "number": 0,
            "first": true,
            "sort": null,
            "numberOfElements": 3
        }
    }
    ```

* add a user 
    * /users/user  -H Content-Type : application/json     POST
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
    "data": {
        "content": [
            {
                "id": 1,
                "name": "tester1",
                "email": "tester1@gmail.com",
                "phone": "1122334455",
                "avatar": null,
                "createTime": null,
                "lastLoginTime": null,
                "jobStatus": null
            },
            {
                "id": 2,
                "name": "tester2",
                "email": "tester2@gmail.com",
                "phone": "1122334455",
                "avatar": null,
                "createTime": null,
                "lastLoginTime": null,
                "jobStatus": null
            },
            {
                "id": 3,
                "name": "tester3",
                "email": "tester3@gmail.com",
                "phone": "1122334455",
                "avatar": null,
                "createTime": null,
                "lastLoginTime": null,
                "jobStatus": null
            },
            {
                "id": 5,
                "name": "tester3",
                "email": "tester11@gmail.com",
                "phone": "778899",
                "avatar": "qq_test3.png",
                "createTime": 1530139223181,
                "lastLoginTime": null,
                "jobStatus": "UNDISTRIBUTED"
            }
        ],
        "last": true,
        "totalElements": 4,
        "totalPages": 1,
        "size": 10,
        "number": 0,
        "first": true,
        "sort": null,
        "numberOfElements": 4
        }
    }
    ```
* update user information 
    * /users/user/{user_id}    -H Content-Type : application/json   PUT
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

* delete user
    * /users/user/{user_id}     DELETE
    ```
    {
    "code": 200,
    "message": null,
    "data": {
        "content": [
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
        ],
        "last": true,
        "totalPages": 1,
        "totalElements": 3,
        "size": 10,
        "number": 0,
        "first": true,
        "sort": null,
        "numberOfElements": 3
        }
    }
    ```

* 
