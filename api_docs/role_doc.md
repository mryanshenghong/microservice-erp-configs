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
        "role_list": {
            "content": [
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
            ],
            "last": true,
            "totalPages": 1,
            "totalElements": 3,
            "size": 10,
            "number": 0,
            "first": true,
            "sort": null,
            "numberOfElements": 3
        },
        "first_role_permissions": {
            "admin": {
                "create": false,
                "update": false,
                "read": false,
                "delete": false
            },
            "inventory": {
                "create": false,
                "update": true,
                "read": true,
                "delete": false
            },
            "user": {
                "create": false,
                "update": false,
                "read": false,
                "delete": false
            }
        },
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