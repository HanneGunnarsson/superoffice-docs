---
title: POST Agents/Project/SaveProjectEventEntity
uid: v1ProjectAgent_SaveProjectEventEntity
---

# POST Agents/Project/SaveProjectEventEntity

```http
POST /api/v1/Agents/Project/SaveProjectEventEntity
```

Updates the existing ProjectEventEntity or creates a new ProjectEventEntity if the id parameter is empty








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

## Request Body: entity 

The ProjectEventEntity to be saved. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| SignOffConfirmationText | String | Text shown as confirmation text before accepting sign off. |
| SignOffText | String | Default text for the activity created when signing off. |
| SignOnConfirmationText | String | Text shown as confirmation text before accepting sign on. |
| SignOnText | String | Default text for the activity created when signing on. |
| EventDate | String | Dateof the event; publishing/visibility dates are in Publish, and restrictions are in AudienceVisibility |
| Enabled | Boolean | Is the event enabled |
| CreatedDate | String | Registered when  in UTC. |
| SignOff | Boolean | Is Sign Off functionality enabled? |
| SignOffTaskEnable | Boolean | If not 0, a task should be created when the external user Signs Off an event |
| SignOffTaskId | Integer | If not 0, sign off should cause an Activity of this type to be registered |
| SignOffTriggersAssign | Boolean | If 1, the SignOff task should be created as an Assigned task, triggering the invitation dialog |
| SignOn | Boolean | Is Sign On functionality enabled |
| SignOnTaskEnable | Boolean | If not 0, a task should be created when the external user Signs On to an event |
| SignOnTaskId | Integer | If not 0, sign on should cause an Activity of this type to be registered |
| SignOnTriggersAssign | Boolean | If 1, the SignOn task should be created as an Assigned task, triggering the invitation dialog |
| UpdatedDate | String | Last updated when  in UTC. |
| CreatedBy | Associate | The person that created the projectevent |
| UpdatedBy | Associate | The person that last updated the projectevent |
| ProjectId | Integer | The projectId for the project this projectEvent belongs to |
| Id | Integer | Id of the external event |
| PublishFrom | String | Publication valid from (inclusive) |
| PublishType | String | Type of publishing action, 0 = Unknown, 1 = to external persons |
| PublishTo | String | Publication valid to (inclusive) |
| VisibleForCategories | Array | Array of categories that the event is visible for. MDO Table "category". |
| VisibleForPersonInterests | Array | Array of person interests (MDO table "persint") that this event is visible for. |
| IsPublished | Boolean | Publish to external users? When true, the event/project information is visible to external users through the Audience portal. You can control the publish duration using the PublishFrom/PublishTo properties. |
| IsVisibleForMembers | Boolean |  |
| IsVisibleForCategories | Boolean |  |
| IsVisibleForPersonInterests | Boolean |  |
| ProjectEventId | Integer | Primary key |

## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: ProjectEventEntity

| Property Name | Type |  Description |
|----------------|------|--------------|
| SignOffConfirmationText | string | Text shown as confirmation text before accepting sign off. |
| SignOffText | string | Default text for the activity created when signing off. |
| SignOnConfirmationText | string | Text shown as confirmation text before accepting sign on. |
| SignOnText | string | Default text for the activity created when signing on. |
| EventDate | date-time | Dateof the event; publishing/visibility dates are in Publish, and restrictions are in AudienceVisibility |
| Enabled | bool | Is the event enabled |
| CreatedDate | date-time | Registered when  in UTC. |
| SignOff | bool | Is Sign Off functionality enabled? |
| SignOffTaskEnable | bool | If not 0, a task should be created when the external user Signs Off an event |
| SignOffTaskId | int32 | If not 0, sign off should cause an Activity of this type to be registered |
| SignOffTriggersAssign | bool | If 1, the SignOff task should be created as an Assigned task, triggering the invitation dialog |
| SignOn | bool | Is Sign On functionality enabled |
| SignOnTaskEnable | bool | If not 0, a task should be created when the external user Signs On to an event |
| SignOnTaskId | int32 | If not 0, sign on should cause an Activity of this type to be registered |
| SignOnTriggersAssign | bool | If 1, the SignOn task should be created as an Assigned task, triggering the invitation dialog |
| UpdatedDate | date-time | Last updated when  in UTC. |
| CreatedBy | Associate | The person that created the projectevent |
| UpdatedBy | Associate | The person that last updated the projectevent |
| ProjectId | int32 | The projectId for the project this projectEvent belongs to |
| Id | int32 | Id of the external event |
| PublishFrom | date-time | Publication valid from (inclusive) |
| PublishType | string | Type of publishing action, 0 = Unknown, 1 = to external persons |
| PublishTo | date-time | Publication valid to (inclusive) |
| VisibleForCategories | array | Array of categories that the event is visible for. MDO Table "category". |
| VisibleForPersonInterests | array | Array of person interests (MDO table "persint") that this event is visible for. |
| IsPublished | bool | Publish to external users? When true, the event/project information is visible to external users through the Audience portal. You can control the publish duration using the PublishFrom/PublishTo properties. |
| IsVisibleForMembers | bool |  |
| IsVisibleForCategories | bool |  |
| IsVisibleForPersonInterests | bool |  |
| ProjectEventId | int32 | Primary key |
| TableRight | TableRight |  |
| FieldProperties | object |  |

## Sample request

```http!
POST /api/v1/Agents/Project/SaveProjectEventEntity
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "SignOffConfirmationText": "libero",
  "SignOffText": "omnis",
  "SignOnConfirmationText": "earum",
  "SignOnText": "dolor",
  "EventDate": "1997-04-10T11:22:38.8208433+02:00",
  "Enabled": false,
  "CreatedDate": "2020-01-28T11:22:38.8208433+01:00",
  "SignOff": true,
  "SignOffTaskEnable": true,
  "SignOffTaskId": 808,
  "SignOffTriggersAssign": false,
  "SignOn": true,
  "SignOnTaskEnable": false,
  "SignOnTaskId": 842,
  "SignOnTriggersAssign": false,
  "UpdatedDate": "2007-03-22T11:22:38.8208433+01:00",
  "CreatedBy": null,
  "UpdatedBy": null,
  "ProjectId": 369,
  "Id": 579,
  "PublishFrom": "2019-08-01T11:22:38.8208433+02:00",
  "PublishType": "External",
  "PublishTo": "1997-03-26T11:22:38.8208433+01:00",
  "VisibleForCategories": [
    {
      "Id": 314,
      "Name": "Dare-Hoppe",
      "ToolTip": "Eum necessitatibus ullam.",
      "Deleted": false,
      "Rank": 67,
      "Type": "explicabo",
      "ChildItems": [
        {},
        {}
      ],
      "IconHint": "autem",
      "ColorBlock": 743,
      "ExtraInfo": "quo",
      "StyleHint": "accusantium",
      "FullName": "Vernon Mraz"
    }
  ],
  "VisibleForPersonInterests": [
    {
      "Id": 150,
      "Name": "Gulgowski Inc and Sons",
      "ToolTip": "Repellendus ex recusandae ut tenetur aut.",
      "Deleted": false,
      "Rank": 550,
      "Type": "aut",
      "ChildItems": [
        {},
        {}
      ],
      "IconHint": "non",
      "ColorBlock": 914,
      "ExtraInfo": "omnis",
      "StyleHint": "eum",
      "FullName": "Asia Abbott"
    }
  ],
  "IsPublished": false,
  "IsVisibleForMembers": false,
  "IsVisibleForCategories": false,
  "IsVisibleForPersonInterests": false,
  "ProjectEventId": 484
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "SignOffConfirmationText": "recusandae",
  "SignOffText": "exercitationem",
  "SignOnConfirmationText": "voluptas",
  "SignOnText": "aut",
  "EventDate": "2019-07-10T11:22:38.8208433+02:00",
  "Enabled": true,
  "CreatedDate": "2016-06-29T11:22:38.8208433+02:00",
  "SignOff": false,
  "SignOffTaskEnable": false,
  "SignOffTaskId": 226,
  "SignOffTriggersAssign": true,
  "SignOn": false,
  "SignOnTaskEnable": true,
  "SignOnTaskId": 1000,
  "SignOnTriggersAssign": false,
  "UpdatedDate": "2004-10-27T11:22:38.8208433+02:00",
  "CreatedBy": null,
  "UpdatedBy": null,
  "ProjectId": 223,
  "Id": 443,
  "PublishFrom": "2014-12-13T11:22:38.8208433+01:00",
  "PublishType": "External",
  "PublishTo": "1997-04-06T11:22:38.8208433+02:00",
  "VisibleForCategories": [
    {
      "Id": 198,
      "Name": "Macejkovic Group",
      "ToolTip": "Praesentium laborum odio accusantium ea.",
      "Deleted": false,
      "Rank": 470,
      "Type": "nisi",
      "ChildItems": [
        {},
        {}
      ],
      "IconHint": "qui",
      "ColorBlock": 939,
      "ExtraInfo": "aliquid",
      "StyleHint": "adipisci",
      "FullName": "General Monahan",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 305
        }
      }
    }
  ],
  "VisibleForPersonInterests": [
    {
      "Id": 57,
      "Name": "Ferry-Steuber",
      "ToolTip": "Voluptatem non aut quibusdam eos.",
      "Deleted": true,
      "Rank": 308,
      "Type": "et",
      "ChildItems": [
        {},
        {}
      ],
      "IconHint": "placeat",
      "ColorBlock": 937,
      "ExtraInfo": "cum",
      "StyleHint": "illum",
      "FullName": "Cesar Witting Jr.",
      "TableRight": null,
      "FieldProperties": {
        "fieldName": {
          "FieldRight": null,
          "FieldType": "System.Int32",
          "FieldLength": 429
        }
      }
    }
  ],
  "IsPublished": true,
  "IsVisibleForMembers": false,
  "IsVisibleForCategories": false,
  "IsVisibleForPersonInterests": true,
  "ProjectEventId": 721,
  "TableRight": null,
  "FieldProperties": {
    "fieldName": {
      "FieldRight": null,
      "FieldType": "System.String",
      "FieldLength": 708
    }
  }
}
```