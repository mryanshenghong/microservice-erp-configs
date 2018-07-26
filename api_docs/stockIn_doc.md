* get all stockIn list
	
	* inventory/stock_in?accept={acceptType}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 555002,
            "batchNo": "B_0123",
            "entryTime": 1483369200000,
            "receiveUserId": 18888,
            "note": "Sample note 1"
        },
        {
            "id": 555003,
            "batchNo": "B_0124",
            "entryTime": 1486137600000,
            "receiveUserId": 18888,
            "note": "Sample note 2"
        },
        {
            "id": 555004,
            "batchNo": "B_0125",
            "entryTime": 1525449600000,
            "receiveUserId": 18888,
            "note": "Sample note 3"
        }
    ]
	}
	```

* get stockIn details

	* inventory/stock_in/{stockInId} 

	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 555002,
        "batchNo": "B_0123",
        "entryTime": 1483369200000,
        "receiveUserId": 18888,
        "note": "Sample note 1"
    }
	}
	```

* get stockIn details by batchNo

	* inventory/stock_in/batch/{batchNo} GET

	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 555003,
        "batchNo": "B_0124",
        "entryTime": 1486137600000,
        "receiveUserId": 18888,
        "note": "Sample note 2"
    }
	}
	```


* get stockIn by commodity ID

	* inventory/stock_in/commodity/{CommodityId}?accept={acceptType}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 555002,
            "batchNo": "B_0123",
            "entryTime": 1483369200000,
            "receiveUserId": 18888,
            "note": "Sample note 1"
        },
        {
            "id": 555003,
            "batchNo": "B_0124",
            "entryTime": 1486137600000,
            "receiveUserId": 18888,
            "note": "Sample note 2"
        }
    ]
	}
	```

* get StockIn By Receiver ID

	* inventory/stock_in/receiver/{receiverId}?accept={acceptType}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 555002,
            "batchNo": "B_0123",
            "entryTime": 1483369200000,
            "receiveUserId": 18888,
            "note": "Sample note 1"
        },
        {
            "id": 555003,
            "batchNo": "B_0124",
            "entryTime": 1486137600000,
            "receiveUserId": 18888,
            "note": "Sample note 2"
        }
    ]
	}
	```

* get stockIn By entry period

	* inventory/stock_in/entry_time?accept={acceptType}&from={fromTime}&to={toTime}&pageNo={pageNo}&pageSize={pageSize} GET
	* defaulet value: accept=list; pageNo=0; pagesize=10; from="2000-01-01 00:00:00"; to=now time

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 555002,
            "batchNo": "B_0123",
            "entryTime": 1483369200000,
            "receiveUserId": 18888,
            "note": "Sample note 1"
        },
        {
            "id": 555003,
            "batchNo": "B_0124",
            "entryTime": 1486137600000,
            "receiveUserId": 18888,
            "note": "Sample note 2"
        },
        {
            "id": 555004,
            "batchNo": "B_0125",
            "entryTime": 1525449600000,
            "receiveUserId": 18886,
            "note": "Sample note 3"
        }
    ]
	}
	```
