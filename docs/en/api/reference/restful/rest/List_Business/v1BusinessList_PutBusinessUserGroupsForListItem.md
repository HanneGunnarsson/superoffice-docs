---
title: PUT List/Business/Items/{id}/UserGroups
uid: v1BusinessList_PutBusinessUserGroupsForListItem
---

# PUT List/Business/Items/{id}/UserGroups

```http
PUT /api/v1/List/Business/Items/{itemId}/UserGroups
```

Saves user groups visible for the Business list's item.


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
PUT /api/v1/List/Business/Items/{itemId}/UserGroups
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: sv
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 747,
    "Name": "Stoltenberg-Leuschke",
    "ToolTip": "Ipsam molestias.",
    "Deleted": true,
    "Rank": 928,
    "Type": "iste",
    "ColorBlock": 833,
    "IconHint": "omnis",
    "Selected": true,
    "LastChanged": "2014-10-27T12:15:27.872622+01:00",
    "ChildItems": [
      {
        "Id": 715,
        "Name": "Kuphal-Cruickshank",
        "ToolTip": "Quis iusto similique aliquid voluptas sint.",
        "Deleted": false,
        "Rank": 255,
        "Type": "omnis",
        "ColorBlock": 506,
        "IconHint": "aut",
        "Selected": false,
        "LastChanged": "2016-03-28T12:15:27.8736229+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "et",
        "StyleHint": "omnis",
        "Hidden": false,
        "FullName": "Rodolfo Mraz"
      }
    ],
    "ExtraInfo": "ea",
    "StyleHint": "ut",
    "Hidden": false,
    "FullName": "Mr. Tomasa Ward Jr."
  }
]
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

[
  {
    "Id": 602,
    "Name": "Jacobson-Rowe",
    "ToolTip": "Suscipit qui dignissimos sunt culpa ratione.",
    "Deleted": true,
    "Rank": 443,
    "Type": "alias",
    "ColorBlock": 744,
    "IconHint": "consequuntur",
    "Selected": false,
    "LastChanged": "2014-07-19T12:15:27.8756227+02:00",
    "ChildItems": [
      {
        "Id": 248,
        "Name": "Larson LLC",
        "ToolTip": "Laboriosam amet dignissimos suscipit est officia error.",
        "Deleted": true,
        "Rank": 187,
        "Type": "voluptatem",
        "ColorBlock": 120,
        "IconHint": "iste",
        "Selected": false,
        "LastChanged": "2005-08-13T12:15:27.8756227+02:00",
        "ChildItems": [
          {},
          {}
        ],
        "ExtraInfo": "ad",
        "StyleHint": "blanditiis",
        "Hidden": false,
        "FullName": "Dr. Missouri Tyree Sawayn",
        "TableRight": null,
        "FieldProperties": {
          "fieldName": {
            "FieldRight": null,
            "FieldType": "System.Int32",
            "FieldLength": 867
          }
        }
      }
    ],
    "ExtraInfo": "non",
    "StyleHint": "magnam",
    "Hidden": true,
    "FullName": "Kole Mosciski I",
    "TableRight": null,
    "FieldProperties": {
      "fieldName": {
        "FieldRight": null,
        "FieldType": "System.String",
        "FieldLength": 872
      }
    }
  }
]
```