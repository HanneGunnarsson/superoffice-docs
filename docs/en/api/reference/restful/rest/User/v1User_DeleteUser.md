---
title: DEL User/{id}
uid: v1User_DeleteUser
---

# DEL User/{id}

```http
DELETE /api/v1/User/{id}
```

Deletes the User


## Online Restricted: ## The User agent is not available in Online by default. User management is not allowed for partner apps. Calls the User agent service DeleteUser.





| Path Part | Type | Description |
|-----------|------|-------------|
| id | int32 | The User to be deleted. **Required** |



## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Accept         | Content-type(s) you would like the response in:  |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |


## Response:

User deleted.

| Response | Description |
|----------------|-------------|
| 204 | User deleted. |

### Response body: RecurrenceInfo


## Sample request

```http!
DELETE /api/v1/User/{id}
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 204 User deleted.
Content-Type: application/json; charset=utf-8

null
```