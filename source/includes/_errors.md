# Errors
> Example
Status-Code: 422 Invalid Request

```json
{
  "message": "Invalid user",
  "code": "invalid",
  "fields": {
  	"id": ["Required"]
  }
}
```

Error responses will have a consistently formed JSON body. The keys may include:

Key | Value
--- | -----
message | Human readable message which corresponds to the client error
code | Underscored delimited string 
fields (optional) | A hash of field names that have validations. This has a value of an array with member strings that describe the specific validation error. 

