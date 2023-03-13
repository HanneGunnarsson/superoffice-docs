---
title: PUT List/Priority/Items/{id}/UserGroups
uid: v1PriorityList_PutPriorityUserGroupsForListItem
---

# PUT List/Priority/Items/{id}/UserGroups

```http
PUT /api/v1/List/Priority/Items/{itemId}/UserGroups
```

Saves user groups visible for the Priority list's item.


Calls the List agent service SaveHeadingsForListItemFromListDefinition.





| Path Part | Type | Description |
|-----------|------|-------------|
| itemId | int32 | The ID of the item to save. **Required** |



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

## Request Body: entities 

The headings to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| Id | Integer | The Id of the ListItem |
| Name | String | The name of the ListItem |
| ToolTip | String | The tooltip of the ListItem |
| Deleted | Boolean | The deleted status of the ListItem |
| Rank | Integer | The rank of the ListItem |
| Type | String | The type of the ListItem. Custom field. |
| ColorBlock | Integer | The color indicator of the ListItem color block |
| IconHint | String | The Icon hint of the ListItem. Custom field. |
| Selected | Boolean | True if the ListItem is selected |
| LastChanged | String | Time of last change. |
| ChildItems | Array | The child items of the SelectableMDOListItem |
| ExtraInfo | String | Extra information added to the ListItem. Could be information such as sort order etc or other meta data. Custom field. |
| StyleHint | String | Style hint indicating, information such as background color etc. Custom field. |
| Hidden | Boolean | True if the ListItem is hidden |
| FullName | String | The name of the ListItem in its context |

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
| TableRight | RecurrenceInfo |  |
| FieldProperties | object |  |

## Sample request

```http!
PUT /api/v1/List/Priority/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: fr,de,ru,zh
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 740,
    "Name": "Wiza, Hodkiewicz and Casper",
    "ToolTip": "Voluptates nulla et.",
    "Deleted": false,
    "Rank": 451,
    "Type": "explicabo",
    "ColorBlock": 246,
    "IconHint": "modi",
    "Selected": false,
    "LastChanged": "2006-03-03T12:15:28.2656167+01:00",
    "ChildItems": [
      {
        "Id": 162,
        "Name": "Walter, Wyman and Nitzsche",
        "ToolTip": "Nesciunt pariatur et sed.",
        "Deleted": false,
        "Rank": 472,
        "Type": "non",
        "ColorBlock": 520,
        "IconHint": "accusantium",
        "Selected": false,
        "LastChanged": "2008-02-07T12:15:28.2666167+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "delectus",
        "StyleHint": "magnam",
        "Hidden": false,
        "FullName": "Randi Emmerich"
      }
    ],
    "ExtraInfo": "dolores",
    "StyleHint": "distinctio",
    "Hidden": false,
    "FullName": "Jayda Muller"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 571,
    "Name": "Jones, Langworth and Quitzon",
    "ToolTip": "Id ut.",
    "Deleted": false,
    "Rank": 608,
    "Type": "veniam",
    "ColorBlock": 219,
    "IconHint": "eum",
    "Selected": true,
    "LastChanged": "2011-10-02T12:15:28.2676167+02:00",
    "ChildItems": [
      {
        "Id": 878,
        "Name": "Leannon Inc and Sons",
        "ToolTip": "Odio nesciunt.",
        "Deleted": true,
        "Rank": 363,
        "Type": "et",
        "ColorBlock": 38,
        "IconHint": "fuga",
        "Selected": true,
        "LastChanged": "2006-04-24T12:15:28.2676167+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "natus",
        "StyleHint": "molestiae",
        "Hidden": true,
        "FullName": "Twila Lynch",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 808
          }
        }
      }
    ],
    "ExtraInfo": "eum",
    "StyleHint": "aut",
    "Hidden": true,
    "FullName": "Ethan Hamill",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 127
      }
    }
  }
]
```