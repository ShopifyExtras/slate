# Locations 

## Get Locations
Receive a list of all your Locations you've added to Zapiet.

### HTTP Request
`GET /services/locations`

## Get Location
Receive a specific Location you have added to Zapiet.

### HTTP Request
`GET /services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to retrieve

## Create Location
Creates a new Location within Zapiet.

### HTTP Request
`POST /services/locations`

## Update Location 
Updates an existing Location within Zapiet.

### HTTP Request
`PUT /services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to update

## Delete Location
Delete an existing Location.

`DELETE /services/locations/#{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the Location to delete