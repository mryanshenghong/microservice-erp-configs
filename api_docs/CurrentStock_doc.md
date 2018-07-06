* get stock items by commodity Id

	* /stock/commodity/{commodityID}/items GET

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "serialId": 1110002,
            "skuNo": "g",
            "itemStatus": "SOLD",
            "costPerItem": 345
        },
        {
            "serialId": 1110003,
            "skuNo": "g",
            "itemStatus": "READY_FOR_PRODUCTION",
            "costPerItem": 345
        }
    ]
	}
	```

* get stock items by stockIn Id

	* /stock/stock_in/{stockInId} GET

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "serialId": 1110004,
            "skuNo": "g",
            "itemStatus": "BROKEN",
            "costPerItem": 678
        }
    ]
	}
	```

* get stock items by batchNO

	/stock/batch/{batchNo} GET

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "serialId": 1110002,
            "skuNo": "g",
            "itemStatus": "SOLD",
            "costPerItem": 345
        },
        {
            "serialId": 1110003,
            "skuNo": "g",
            "itemStatus": "READY_FOR_PRODUCTION",
            "costPerItem": 345
        }
    ]
	}
	```

* get items history snapshot
	
	/stock/snapshot?timestamp={timeStamp} GET

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "serialId": 1110002,
            "skuNo": "g",
            "itemStatus": "SOLD",
            "costPerItem": 345
        },
        {
            "serialId": 1110003,
            "skuNo": "g",
            "itemStatus": "READY_FOR_PRODUCTION",
            "costPerItem": 345
        },
        {
            "serialId": 1110004,
            "skuNo": "g",
            "itemStatus": "BROKEN",
            "costPerItem": 678
        },
        {
            "serialId": 1110006,
            "skuNo": "g",
            "itemStatus": "SOLD",
            "costPerItem": 678
        }
    ]
	}
	```