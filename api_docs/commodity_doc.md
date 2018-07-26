* get all commodity list

	* inventory/commodity GET

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 96743,
            "name": "Samsung S7",
            "commodityType": "RAW_MATERIAL",
            "quantityUnit": "10",
            "processingPeriod": 3
        },
        {
            "id": 96746,
            "name": "Samsun S8",
            "commodityType": "PRODUCTION",
            "quantityUnit": "7",
            "processingPeriod": 9
        }
    ]
	}
	```

* is commodity existed by name

	* inventory/commodity/name/{commodityName} GET

	```
	{
    "code": 200,
    "message": null,
    "data": true
	}
	```

* delete one commodity 

	* inventory/commodity/{commodityId} DELETE

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 96743,
            "name": "Samsung S7",
            "commodityType": "RAW_MATERIAL",
            "quantityUnit": "10",
            "processingPeriod": 3
        }
    ]
	}
	```

* display commodity in list only include id and name field

	* inventory/commodity OPTION

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 96743,
            "name": "Samsung S7"
        },
        {
            "id": 96746,
            "name": "Samsun S8"
        }
    ]
	}
	```

* create an comodity

	* inventory/commotidy -H Content-Type : application/json POST
	* name : not null; commodityType : not null; 

	```
	{
		"name": "Samsung S10",
		"commodityType": "RAW_MATERIAL",
		"quantityUnit": "10",
		"processingPeriod": 3
	}
	```

	```
	{
    "code": 200,
    "message": null,
    "data": [
        {
            "id": 96743,
            "name": "Samsung S7",
            "commodityType": "RAW_MATERIAL",
            "quantityUnit": "10",
            "processingPeriod": 3
        },
        {
            "id": 96746,
            "name": "Samsun S8",
            "commodityType": "PRODUCTION",
            "quantityUnit": "7",
            "processingPeriod": 9
        },
        {
            "id": 98657,
            "name": "Samsung S10",
            "commodityType": "RAW_MATERIAL",
            "quantityUnit": "10",
            "processingPeriod": 3
        }
    ]
	}
	```

* update commodity info

	* inventory/commodity/{commodityId} -H Content-Type : application/json POST
	* id : not null;

	```
	{
        "name": "Samsung S11",
        "commodityType": "PRODUCTION",
        "quantityUnit": "3",
        "processingPeriod": 1
    }
	```

	```
	{
    "code": 200,
    "message": null,
    "data": {
        "id": 98654,
        "name": "Samsung Duo",
        "commodityType": "RAW_MATERIAL",
        "quantityUnit": "18",
        "processingPeriod": 8
    }
	}
	```
