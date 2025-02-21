---
title: PUT List/ProductCategory/Items/{id}/Headings
uid: v1ProductCategoryList_PutProductCategoryHeadingsForListItem
---

# PUT List/ProductCategory/Items/{id}/Headings

```http
PUT /api/v1/List/ProductCategory/Items/{itemId}/Headings
```

Saves headings for the ProductCategory list's item.


Calls the List agent service SaveHeadingsForListItemFromListDefinition.





| Path Part | Type | Description |
|-----------|------|-------------|
| itemId | int32 | The ID of the headings to be saved. **Required** |



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
PUT /api/v1/List/ProductCategory/Items/{itemId}/Headings
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 601,
    "Name": "Lebsack, Spencer and Heathcote",
    "ToolTip": "Explicabo facilis autem autem velit omnis omnis et.",
    "Deleted": false,
    "Rank": 792,
    "Type": "voluptas",
    "ColorBlock": 138,
    "IconHint": "earum",
    "Selected": false,
    "LastChanged": "2002-04-30T12:15:28.2876167+02:00",
    "ChildItems": [
      {
        "Id": 244,
        "Name": "Hansen, Treutel and Daniel",
        "ToolTip": "Aut saepe illum nam repellat mollitia.",
        "Deleted": true,
        "Rank": 67,
        "Type": "voluptatibus",
        "ColorBlock": 710,
        "IconHint": "voluptas",
        "Selected": false,
        "LastChanged": "1997-02-17T12:15:28.2876167+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "placeat",
        "StyleHint": "totam",
        "Hidden": true,
        "FullName": "Dr. Elouise Queenie Botsford PhD"
      }
    ],
    "ExtraInfo": "explicabo",
    "StyleHint": "incidunt",
    "Hidden": false,
    "FullName": "Dorothea Greenholt"
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 131,
    "Name": "Bednar, Howell and Homenick",
    "ToolTip": "Unde quisquam explicabo dolores qui eos.",
    "Deleted": true,
    "Rank": 892,
    "Type": "et",
    "ColorBlock": 287,
    "IconHint": "nesciunt",
    "Selected": false,
    "LastChanged": "2020-04-28T12:15:28.288617+02:00",
    "ChildItems": [
      {
        "Id": 523,
        "Name": "Brown, McLaughlin and Beier",
        "ToolTip": "At quia est necessitatibus voluptas quia unde natus.",
        "Deleted": true,
        "Rank": 520,
        "Type": "voluptas",
        "ColorBlock": 92,
        "IconHint": "ratione",
        "Selected": false,
        "LastChanged": "2005-01-03T12:15:28.288617+01:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "incidunt",
        "StyleHint": "id",
        "Hidden": false,
        "FullName": "Marquise McKenzie Sr.",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 164
          }
        }
      }
    ],
    "ExtraInfo": "nostrum",
    "StyleHint": "non",
    "Hidden": true,
    "FullName": "Columbus Parker",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.String",
        "FieldLength": 798
      }
    }
  }
]
```