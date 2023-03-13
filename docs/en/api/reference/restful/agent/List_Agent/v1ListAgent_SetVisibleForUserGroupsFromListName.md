---
title: POST Agents/List/SetVisibleForUserGroupsFromListName
uid: v1ListAgent_SetVisibleForUserGroupsFromListName
---

# POST Agents/List/SetVisibleForUserGroupsFromListName

```http
POST /api/v1/Agents/List/SetVisibleForUserGroupsFromListName
```

Update User groups that this list item is visible for







## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| $select | string |  Optional comma separated list of properties to include in the result. Other fields are then nulled out to reduce payload size: "Name,department,category". Default = show all fields. |

```http
POST /api/v1/Agents/List/SetVisibleForUserGroupsFromListName?$select=name,department,category/id
```


## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Content-Type | Content-type of the request body: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |

## Request Body: request 

UdListDefinitionName, ListItemId, UserGroups 

| Property Name | Type |  Description |
|----------------|------|--------------|
| UdListDefinitionName | String |  |
| ListItemId | Integer |  |
| UserGroups | Array |  |

## Response:array

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: array

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | int32 | The Id of the ListItem |
| Name | string | The name of the ListItem |
| ToolTip | string | The tooltip of the ListItem |
| Deleted | bool | The deleted status of the ListItem |
| Rank | int32 | The rank of the ListItem |
| Type | string | The type of the ListItem. Custom field. |
| ColorBlock | int32 | The color indicator of the ListItem color block |
| IconHint | string | The Icon hint of the ListItem. Custom field. |
| Selected | bool | True if the ListItem is selected |
| LastChanged | date-time | Time of last change. |
| ChildItems | array | The child items of the SelectableMDOListItem |
| ExtraInfo | string | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | string | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | bool | True if the ListItem is hidden |
| FullName | string | The name of the ListItem in its context |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/List/SetVisibleForUserGroupsFromListName
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "UdListDefinitionName": "Simonis, Walter and Prohaska",
  "ListItemId": 955,
  "UserGroups": [
    {
      "Id": 691,
      "Name": "Carter-McCullough",
      "ToolTip": "Quis omnis non ea.",
      "Deleted": true,
      "Rank": 867,
      "Type": "nisi",
      "ColorBlock": 760,
      "IconHint": "facere",
      "Selected": false,
      "LastChanged": "2001-02-22T12:15:19.2507472+01:00",
      "ChildItems": [
        {},
        {}
      ],
      "ExtraInfo": "atque",
      "StyleHint": "modi",
      "Hidden": false,
      "FullName": "Jane Conn"
    }
  ]
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 768,
    "Name": "Lakin, Collier and Bergnaum",
    "ToolTip": "Architecto non deserunt est voluptatem eligendi est officia.",
    "Deleted": false,
    "Rank": 555,
    "Type": "vero",
    "ColorBlock": 482,
    "IconHint": "tempore",
    "Selected": false,
    "LastChanged": "2008-09-20T12:15:19.252755+02:00",
    "ChildItems": [
      {
        "Id": 51,
        "Name": "Spencer, Stokes and Considine",
        "ToolTip": "Molestias sit ullam.",
        "Deleted": true,
        "Rank": 524,
        "Type": "dicta",
        "ColorBlock": 678,
        "IconHint": "et",
        "Selected": false,
        "LastChanged": "2007-10-25T12:15:19.252755+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "voluptates",
        "StyleHint": "perferendis",
        "Hidden": false,
        "FullName": "Miss Olen Zulauf",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.String",
            "FieldLength": 154
          }
        }
      }
    ],
    "ExtraInfo": "vitae",
    "StyleHint": "dignissimos",
    "Hidden": false,
    "FullName": "Xzavier Bradly Lehner V",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.String",
        "FieldLength": 371
      }
    }
  }
]
```