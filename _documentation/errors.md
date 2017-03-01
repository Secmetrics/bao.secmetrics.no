---
title: Errors
position: 4
---

| Code | Name                  | Description                          |
|------|-----------------------|--------------------------------------|
| 200  | Success               | The request was performed successful |
| 400  | Bad Request           | We couldn't process the request      |
| 401  | Unauthorized          | We couldn’t authenticate the request |
| 404  | Not Found             | We couldn’t find the resource        |
| 500  | Internal Server Error | A server error occurred              |

All error response will return JSON as the following example formats:

~~~ json
{
  "code": 200,
  "message": "The URL was valid"
}

{
  "code": 401,
  "message": "Session expired"
}

{
  "code": 404,
  "message": "Return URL not found"
}
~~~
