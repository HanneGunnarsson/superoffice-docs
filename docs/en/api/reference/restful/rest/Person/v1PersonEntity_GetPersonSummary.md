---
title: GET Person/{id}/Summary
uid: v1PersonEntity_GetPersonSummary
---

# GET Person/{id}/Summary

```http
GET /api/v1/Person/{personId}/Summary
```

Get summary of person and recent activity.






| Path Part | Type | Description |
|-----------|------|-------------|
| personId | int32 | The person id to summarize. **Required** |


## Query String Parameters

| Parameter Name | Type |  Description |
|----------------|------|--------------|
| limit | int32 |  Max number of items to include in summary lists. |

```http
GET /api/v1/Person/{personId}/Summary?limit=854
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


## Response:

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: PersonSummary

| Property Name | Type |  Description |
|----------------|------|--------------|
| Person | Person | Simple Person data. |
| Tickets | array | Recent tickets on person |
| Followups | array | Recent follow-ups on person |
| Documents | array | Recent documents on person |
| Sales | array | Recent sales on person |
| Chats | array | Recent chats with person |

## Sample request

```http!
GET /api/v1/Person/{personId}/Summary
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "Person": null,
  "Tickets": [
    {
      "TicketId": 315,
      "TicketStatus": 406,
      "Title": "commodi",
      "Registered": "2022-12-07T11:22:44.9756457+01:00",
      "IconHint": "et"
    },
    {
      "TicketId": 315,
      "TicketStatus": 406,
      "Title": "commodi",
      "Registered": "2022-12-07T11:22:44.9756457+01:00",
      "IconHint": "et"
    }
  ],
  "Followups": [
    {
      "AppointmentId": 704,
      "DocumentId": 418,
      "Date": "2007-06-25T11:22:44.9756457+02:00",
      "Description": "Virtual stable archive",
      "Completed": "Completed",
      "Registered": "2015-03-28T11:22:44.9756457+01:00"
    },
    {
      "AppointmentId": 704,
      "DocumentId": 418,
      "Date": "2007-06-25T11:22:44.9756457+02:00",
      "Description": "Virtual stable archive",
      "Completed": "Completed",
      "Registered": "2015-03-28T11:22:44.9756457+01:00"
    }
  ],
  "Documents": [
    {
      "AppointmentId": 435,
      "DocumentId": 495,
      "Date": "2021-05-28T11:22:44.9756457+02:00",
      "Description": "Re-engineered bifurcated task-force",
      "Completed": "Completed",
      "Registered": "2021-03-09T11:22:44.9756457+01:00"
    },
    {
      "AppointmentId": 435,
      "DocumentId": 495,
      "Date": "2021-05-28T11:22:44.9756457+02:00",
      "Description": "Re-engineered bifurcated task-force",
      "Completed": "Completed",
      "Registered": "2021-03-09T11:22:44.9756457+01:00"
    }
  ],
  "Sales": [
    {
      "SaleId": 148,
      "SaleDate": "2007-09-01T11:22:44.9756457+02:00",
      "Probability": 140,
      "Heading": "nisi",
      "Amount": 13614.096,
      "Currency": "dignissimos",
      "AmountInBaseCurrency": 10091.48,
      "Status": "Lost",
      "Completed": "Completed",
      "Registered": "2011-09-08T11:22:44.9756457+02:00"
    }
  ],
  "Chats": [
    {
      "ChatSessionId": 775,
      "Name": "Hansen-Fadel",
      "CompanyName": "Brown-Strosin",
      "FirstMessage": "consectetur",
      "LastMessage": "eos",
      "WhenRequested": "2012-05-03T11:22:44.9756457+02:00",
      "WhenEnded": "2001-01-31T11:22:44.9756457+01:00"
    }
  ]
}
```