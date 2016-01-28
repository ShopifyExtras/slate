# HTTP Status Codes
Status Code | Description
----------- | -----------
200 | OK<br>Everything worked as expected
201 | Created<br>We will return a 201 after a successful POST where a resource was created
400 | Malformed request
401 | Unauthorized request
403 | Forbidden request
404 | Not found
422 | Invalid Request<br>The request body is parse-able however with invalid content
429 | Too many requests<br>Rate limited
500 | Internal Server Error