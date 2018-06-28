* get role details
	* /users/role/{role_id} 	GET
	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 1,
        "role": "admin",
        "description": "admin account"
	    }
	}
	```

* get role list
	* /users/role 		GET
	```
	{
    "code": 200,
    "message": null,
    "data": {
        "role_list": [
            {
                "id": 1,
                "role": "admin",
                "description": "admin account"
            },
            {
                "id": 2,
                "role": "staff",
                "description": "staff account"
            },
            {
                "id": 3,
                "role": "manager",
                "description": "manager account"
            },
            {
                "id": 4,
                "role": "admin_assistant",
                "description": "admin assistant"
            }
        ],
        "module_list": [
            {
                "id": 1,
                "name": "user"
            },
            {
                "id": 2,
                "name": "inventory"
            },
            {
                "id": 101,
                "name": "admin"
            }
        ]
        }
    }
	```
* add role
	* /users/role 		POST
    * role(name) : not null
	```
	{
    "role": "admin_assistant",
    "description": "admin assistant"
	}
	```
	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 1,
            "role": "admin",
            "description": "admin account"
        },
        {
            "id": 2,
            "role": "staff",
            "description": "staff account"
        },
        {
            "id": 3,
            "role": "manager",
            "description": "manager account"
        },
        {
            "id": 4,
            "role": "admin_assistant",
            "description": "admin assistant"
        }
	    ]
	}
	```

* update the details of role 
    * /users/role/{role_id}     PUT
    * role : not null
    ```
    {
    "role": "admin_assistant",
    "description": "admin assistant 0"
    }
    ```
    ```
    {
    "code": 200,
    "message": null,
    "data": {
        "id": 4,
        "role": "admin_assistant",
        "description": "admin assistant 0"
        }
    }
    ```
* delete role
    * /users/role/{role_id}         DELETE
    ```
    {
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 1,
            "role": "admin",
            "description": "admin account"
        },
        {
            "id": 2,
            "role": "staff",
            "description": "staff account"
        },
        {
            "id": 3,
            "role": "manager",
            "description": "manager account"
        }
        ]
    }
    ```

* get details of permissions about one role
    * /users/role/{role_id}/permissions         GET
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