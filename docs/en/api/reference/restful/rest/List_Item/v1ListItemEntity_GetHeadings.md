---
title: GET List/{id}/Items/{id}/Headings
uid: v1ListItemEntity_GetHeadings
---

# GET List/{id}/Items/{id}/Headings

```http
GET /api/v1/List/{udListDefinitionId}/Items/{listItemId}/Headings
```

Gets a selectable MDO list of the headings for this list item






| Path Part | Type | Description |
|-----------|------|-------------|
| udListDefinitionId | int32 | The id of the list. Negative numbers indicate TableNumber value instead of UDListDefId. e.g. -64 = category. **Required** |
| listItemId | int32 | The id of the list item **Required** |


## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| showDeleted | bool |  Set to true if you want deleted headings |

```http
GET /api/v1/List/{udListDefinitionId}/Items/{listItemId}/Headings?showDeleted=False
```


## Request Headers

| Parameter Name | Description |
|----------------|-------------|
| Authorization  | Supports 'Basic', 'SoTicket' and 'Bearer' schemes, depending on installation type. |
| X-XSRF-TOKEN   | If not using Authorization header, you must provide XSRF value from cookie or hidden input field |
| Accept         | Content-type(s) you would like the response in: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/json-patch+json`, `application/merge-patch+json` |
| Accept-Language | Convert string references and multi-language values into a specified language (iso2) code. |
| SO-Language | Convert string references and multi-language values into a specified language (iso2) code. Overrides Accept-Language value. |
| SO-Culture | Number, date formatting in a specified culture (iso2 language) code. Partially overrides SO-Language/Accept-Language value. Ignored if no Language set. |
| SO-TimeZone | Specify the timezone code that you would like date/time responses converted to. |
| SO-AppToken | The application token that identifies the partner app. Used when calling Online WebAPI from a server. |


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
GET /api/v1/List/{udListDefinitionId}/Items/{listItemId}/Headings
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 780,
    "Name": "Schmidt Inc and Sons",
    "ToolTip": "Ad rerum vero est omnis facere.",
    "Deleted": false,
    "Rank": 814,
    "Type": "quia",
    "ColorBlock": 421,
    "IconHint": "et",
    "Selected": false,
    "LastChanged": "2018-12-03T11:22:45.5692589+01:00",
    "ChildItems": [
      {
        "Id": 348,
        "Name": "Rohan-White",
        "ToolTip": "Sit nulla itaque quibusdam.",
        "Deleted": false,
        "Rank": 871,
        "Type": "et",
        "ColorBlock": 375,
        "IconHint": "recusandae",
        "Selected": false,
        "LastChanged": "2012-01-19T11:22:45.5692589+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "mollitia",
        "StyleHint": "possimus",
        "Hidden": false,
        "FullName": "Aglae Glover",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 392
          }
        }
      }
    ],
    "ExtraInfo": "voluptatem",
    "StyleHint": "perferendis",
    "Hidden": false,
    "FullName": "Mr. Ottis Addie Lowe",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.Int32",
        "FieldLength": 559
      }
    }
  }
]
```