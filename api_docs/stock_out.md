* get all stockOut

	* /stock_out?accept={acceptType}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666001,
            "pickedTime": 1531445725000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "CLEANING",
            "note": "Sent for cleaning"
        },
        {
            "id": 666002,
            "pickedTime": 1532136929000,
            "pickedUser": 16789,
            "approvedUser": 1456,
            "purpose": "SELL",
            "note": "Sent"
        },
        {
            "id": 666003,
            "pickedTime": 1532050532000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "PROCESS",
            "note": "For Processing "
        }
    ]
	}
	```

* get stockOut details by stockOut ID

	* /stock_out/{stockOutId} GET

	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 666002,
        "pickedTime": 1532136929000,
        "pickedUser": 16789,
        "approvedUser": 1456,
        "purpose": "SELL",
        "note": "Sent"
    }
	}
	```

* get stockOut details by item ID

	* /stock_out/item/{itemId}

	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 666002,
        "pickedTime": 1532136929000,
        "pickedUser": 16789,
        "approvedUser": 1456,
        "purpose": "SELL",
        "note": "Sent"
    }
	```

* get stockOut list by pickout period 

	* /stock_out/picked_time?accept={acceptType}&from={fromTime}&to={toTime}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10; from="2000-01-01 00:00:00"; to=now time

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666001,
            "pickedTime": 1531445725000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "CLEANING",
            "note": "Sent for cleaning"
        },
        {
            "id": 666002,
            "pickedTime": 1532136929000,
            "pickedUser": 16789,
            "approvedUser": 1456,
            "purpose": "SELL",
            "note": "Sent"
        },
        {
            "id": 666003,
            "pickedTime": 1532050532000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "PROCESS",
            "note": "For Processing "
        }
    ]
	}
	```

* get stockOut by picked purpose
	
	* /stock_out/purpose?accept={acceptType}&purpose={purpose}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10;

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666002,
            "pickedTime": 1532136929000,
            "pickedUser": 16789,
            "approvedUser": 1456,
            "purpose": "SELL",
            "note": "Sent"
        }
    ]
	}
	```


* get stockOut by picked user id

	* /stock_out/pick_user?accept={acceptType}&pick_user={pickUserId}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10;

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666002,
            "pickedTime": 1532136929000,
            "pickedUser": 16788,
            "approvedUser": 1456,
            "purpose": "SELL",
            "note": "Sent"
        }
    ]
	}
	```

* get stockOut by approved user id 

	* /stock_out/approve_user?accept={acceptType}&approve_user={approveUserId}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10;

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666001,
            "pickedTime": 1531445725000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "CLEANING",
            "note": "Sent for cleaning"
        },
        {
            "id": 666003,
            "pickedTime": 1532050532000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "PROCESS",
            "note": "For Processing "
        }
    ]
	}
	```

* get stockOut by custome criterion
	
	* /stock_out/~cirterion?accept={acceptType}&pageNo={pageNo}&pageSize={pageSize} POST
	* Request body: HashMap -> custome critetion
	* defaulet value: accept=list; pageNo=0; pagesize=10;

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 666001,
            "pickedTime": 1531445725000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "CLEANING",
            "note": "Sent for cleaning"
        },
        {
            "id": 666003,
            "pickedTime": 1532050532000,
            "pickedUser": 16789,
            "approvedUser": 1234,
            "purpose": "PROCESS",
            "note": "For Processing "
        }
    ]
	}
	```