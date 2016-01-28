# Accounts 

## Get Accounts
Receive a list of all Accounts which have your services installed.

### HTTP Request
`GET /services/accounts`

## Get Account
Receive a single Account.

### HTTP Request
`GET /services/accounts/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Account to retrieve

## Activate
Activates your services on the specific Account.

### HTTP Request
`POST /services/accounts/#{id}/activate`

### Query Parameters

Parameter | Description
--------- | -----------
id | The ID of the Account you wish to activate your services on

## Deactivate
Deactivates your service on a specific Account.

### HTTP Request
`POST /services/accounts/#{id}/deactivate`

### Query Parameters

Parameter | Description
--------- | -----------
account_id | The ID of the Account account you wish to remove your services from