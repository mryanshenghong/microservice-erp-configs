* login
	* auth/oauth/token   -H Accept:application/json  -H content-type: application/x-www-formurlencoded
	* Authorization Basic username:angular_app; Password:ERP!@#angular
		* (if Angular can not support) -H Authorization: Basic YW5ndWxhcl9hcHA6RVJQIUAjYW5ndWxhcg==
	* form-data:
	```
	grant_type: password
	username: {user_name}
	password: {password}
	scope: angular_app
	```
	* repsonse:
	```
	{
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoxLCJ1c2VyX25hbWUiOiJ0ZXN0ZXIxQGdtYWlsLmNvbSIsInNjb3BlIjpbImFuZ3VsYXJfYXBwIl0sImV4cCI6MTUzMDI0NTIyMCwiYXV0aG9yaXRpZXMiOlsidXNlcl9DUkVBVEUiLCJ1c2VyX1VQREFURSIsInVzZXJfREVMRVRFIiwidXNlcl9SRUFEIl0sImp0aSI6IjVlMDZhNzFkLTIxNWYtNGMzOS1iNzU1LTAzYjFmZTQ2OTg2NCIsImNsaWVudF9pZCI6ImFuZ3VsYXJfYXBwIn0.Z0ZCycbt4tqlrDt-oIXpG0BetRRKZbaFM6B_Rf-5Ibk",
    "token_type": "bearer",
    "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoxLCJ1c2VyX25hbWUiOiJ0ZXN0ZXIxQGdtYWlsLmNvbSIsInNjb3BlIjpbImFuZ3VsYXJfYXBwIl0sImF0aSI6IjVlMDZhNzFkLTIxNWYtNGMzOS1iNzU1LTAzYjFmZTQ2OTg2NCIsImV4cCI6MTUzMjc5NDAyMCwiYXV0aG9yaXRpZXMiOlsidXNlcl9DUkVBVEUiLCJ1c2VyX1VQREFURSIsInVzZXJfREVMRVRFIiwidXNlcl9SRUFEIl0sImp0aSI6IjBhZTIyNTRiLWYyNTItNDNmMi1hZTc0LTIzYWVkNzVmNGY4YiIsImNsaWVudF9pZCI6ImFuZ3VsYXJfYXBwIn0.8S8dKiw9KDWi1t27wf1i1VMwfGGlmlXY_1hem99Yfi8",
    "expires_in": 43199,
    "scope": "angular_app",
    "user_id": 1,
    "jti": "5e06a71d-215f-4c39-b755-03b1fe469864"
	}
	```
