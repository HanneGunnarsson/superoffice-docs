---
title: PUT List/{udListDefinitionName}/Items/{id}/UserGroups
uid: v1ListItemEntity_SetVisibleForUserGroupsFromListName
---

# PUT List/{udListDefinitionName}/Items/{id}/UserGroups

```http
PUT /api/v1/List/{udListDefinitionName}/Items/{listItemId}/UserGroups
```

Update User groups that this list item is visible for






| Path Part | Type | Description |
|-----------|------|-------------|
| udListDefinitionName | string | The name of the list definition, indicating which list to update the items from. **Required** |
| listItemId | int32 | The id of the list item **Required** |



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

## Request Body: userGroups 

The selectable user groups. 

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
PUT /api/v1/List/{udListDefinitionName}/Items/{listItemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 578,
    "Name": "Gislason Inc and Sons",
    "ToolTip": "Laborum esse et quas.",
    "Deleted": false,
    "Rank": 133,
    "Type": "debitis",
    "ColorBlock": 131,
    "IconHint": "fugit",
    "Selected": false,
    "LastChanged": "2016-09-04T12:15:27.8386228+02:00",
    "ChildItems": [
      {
        "Id": 23,
        "Name": "Goodwin, Waters and Nicolas",
        "ToolTip": "Est consequatur id expedita illo ducimus.",
        "Deleted": false,
        "Rank": 429,
        "Type": "dolore",
        "ColorBlock": 229,
        "IconHint": "reiciendis",
        "Selected": false,
        "LastChanged": "2021-04-18T12:15:27.8386228+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "rerum",
        "StyleHint": "omnis",
        "Hidden": false,
        "FullName": "Ladarius Beer"
      }
    ],
    "ExtraInfo": "rem",
    "StyleHint": "ducimus",
    "Hidden": false,
    "FullName": "Ellen Jewel Jast IV"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 708,
    "Name": "Kihn, Koch and Kohler",
    "ToolTip": "Odit beatae voluptas et et assumenda iste eos.",
    "Deleted": true,
    "Rank": 167,
    "Type": "consequatur",
    "ColorBlock": 593,
    "IconHint": "eos",
    "Selected": false,
    "LastChanged": "2015-02-10T12:15:27.8396227+01:00",
    "ChildItems": [
      {
        "Id": 622,
        "Name": "Lakin-Harris",
        "ToolTip": "Error architecto.",
        "Deleted": false,
        "Rank": 294,
        "Type": "omnis",
        "ColorBlock": 230,
        "IconHint": "aliquam",
        "Selected": false,
        "LastChanged": "2015-12-09T12:15:27.8406237+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "libero",
        "StyleHint": "cum",
        "Hidden": false,
        "FullName": "Ms. Blaise Strosin III",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 128
          }
        }
      }
    ],
    "ExtraInfo": "aperiam",
    "StyleHint": "placeat",
    "Hidden": false,
    "FullName": "Lavada Veum",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 442
      }
    }
  }
]
```