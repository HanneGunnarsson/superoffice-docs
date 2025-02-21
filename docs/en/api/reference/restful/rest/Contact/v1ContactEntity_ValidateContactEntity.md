---
title: POST Contact/Validate
uid: v1ContactEntity_ValidateContactEntity
---

# POST Contact/Validate

```http
POST /api/v1/Contact/Validate
```

Check that entity is ready for saving, return error messages by field.








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

## Request Body: contactEntity 

Entity to be checked for errors. 

| Property Name | Type |  Description |
|----------------|------|--------------|
| ContactId | Integer | Primary key |
| Name | String | Contact name |
| Department | String | Department |
| OrgNr | String | VAT number or similar |
| Number1 | String | Alphanumeric user field |
| Number2 | String | Alphanumeric user field |
| UpdatedDate | String | Date last updated  in UTC. |
| CreatedDate | String | Date registered  in UTC. |
| Emails | Array | The contact's email |
| Interests | Array | The contact's available and selected interests.  <para>Use MDO List name "contint" to get list items.</para> |
| Urls | Array | The contact's internet adresses |
| Phones | Array | The contact's phone numbers |
| Faxes | Array | The contact's fax numbers |
| Description | String | Description of the contact. Usually shown as a postit note. |
| UpdatedBy | Associate | The user that last updated the contact |
| CreatedBy | Associate | The user that created the contact |
| Associate | Associate | The user that owns this contact.  <para>Use MDO List name "associate" to get list items.</para> |
| Business | Business | The business that the contact is associated with. The GUI forces the user to enter a business type.  <para>Use MDO List name "business" to get list items.</para> |
| Category | Category | The category that is set on the company. The GUI forces the user to enter a category type  <para>Use MDO List name "category" to get list items.</para> |
| Country | Country | The country this contact is located in. The country a contact is saved with, affects the phone number format, and the address layout.  <para>Use MDO List name "country" to get list items.</para> |
| Persons | Array | The persons belonging to the contact. |
| NoMailing | Boolean | Spam filter. Indicates if this contact should retrieve advertising. |
| Kananame | String | Contact kana name, used in Japanese versions only |
| Xstop | Boolean | STOP flag |
| ActiveInterests | Integer | The number of active interests. |
| GroupId | Integer | Group id of original owning associate, semantics like appnt.grp_id |
| ActiveStatusMonitorId | Integer | Active status monitor identity with the lowest rank for contact |
| SupportAssociate | Associate | <para>Use MDO List name "associate" to get list items.</para> |
| TicketPriority | TicketPriority | <para>Use MDO List name "ticketpriority" to get list items.</para> |
| CustomerLanguage | CustomerLanguage | customerlanguage |
| Deleted | Integer | If nonzero, then this contact is 'deleted' and should generally not be shown |
| DbiAgentId | Integer | Integration agent (eJournal) |
| DbiLastSyncronized | String | Last external syncronization. |
| DbiKey | String | The primary key for the integrated entry in the external datasource. |
| DbiLastModified | String | When the entry was last modified. |
| SupportPerson | Person | Carrier object for Person. Services for the Person Carrier is available from the <see cref="T:SuperOffice.CRM.Services.IPersonAgent">Person Agent</see>. |
| Address | Address | Street and/or Postal address, in both formatted and structured forms. You only need to modify one of the two for the change to be registered. <para /> Carrier object for Address. |
| Source | Integer | How did we get this contact? For future integration needs |
| ActiveErpLinks | Integer | The number of active erp links |
| BounceEmails | Array | Email addresses with a positive bounce counter. |
| Domains | Array | Web domains for this contact, ordered in array by rank |
| UserDefinedFields | Object | Deprecated: Use {SuperOffice.CRM.Services.ContactEntity.CustomFields} instead. Dictionary of user defined field data. The key string is the ProgId of the UdefField, or if the ProgId is empty it is a string of the format "SuperOffice:[UdefFieldIdentity]", e.g. "SuperOffice:1234" |
| ExtraFields | Object | Deprecated: Use {SuperOffice.CRM.Services.ContactEntity.CustomFields} instead. Extra fields added to the carrier. This could be data from Plug-ins, the foreign key system, external applications, etc. |
| CustomFields | Object | Udef + Extra fields added to the carrier. Extra fields as defined by changes to database schema + user-defined fields as defined by admin. Custom fields combines user defined fields and extra fields into one bucket.  The individual {SuperOffice.CRM.Services.ContactEntity.ExtraFields} and <see cref="P:SuperOffice.CRM.Services.ContactEntity.UserDefinedFields">UserDefinedFields</see> properties are deprecated in favor of this combined collection. |

## Response:object

OK

| Response | Description |
|----------------|-------------|
| 200 | OK |

### Response body: object


## Sample request

```http!
POST /api/v1/Contact/Validate
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: en
Content-Type: application/json; charset=utf-8

{
  "ContactId": 215,
  "Name": "Morar, Mante and Mayer",
  "Department": "",
  "OrgNr": "756046",
  "Number1": "1540601",
  "Number2": "1286793",
  "UpdatedDate": "2023-02-01T12:15:26.7706452+01:00",
  "CreatedDate": "2022-11-23T12:15:26.7706452+01:00",
  "Emails": [
    {
      "Value": "ab",
      "StrippedValue": "est",
      "Description": "Re-engineered multi-tasking algorithm"
    },
    {
      "Value": "ab",
      "StrippedValue": "est",
      "Description": "Re-engineered multi-tasking algorithm"
    }
  ],
  "Interests": [
    {
      "Id": 121,
      "Name": "Sawayn-Bartell",
      "ToolTip": "Voluptas consequuntur praesentium nihil.",
      "Deleted": false,
      "Rank": 590,
      "Type": "sit",
      "ColorBlock": 819,
      "IconHint": "alias",
      "Selected": false,
      "LastChanged": "1998-11-19T12:15:26.7706452+01:00",
      "ChildItems": [
        {},
        {}
      ],
      "ExtraInfo": "eos",
      "StyleHint": "nesciunt",
      "Hidden": false,
      "FullName": "Karen Wisoky"
    }
  ],
  "Urls": [
    {
      "Value": "sed",
      "StrippedValue": "corrupti",
      "Description": "Assimilated object-oriented definition"
    },
    {
      "Value": "sed",
      "StrippedValue": "corrupti",
      "Description": "Assimilated object-oriented definition"
    }
  ],
  "Phones": [
    {
      "Value": "repellat",
      "StrippedValue": "sunt",
      "Description": "Total homogeneous approach"
    },
    {
      "Value": "repellat",
      "StrippedValue": "sunt",
      "Description": "Total homogeneous approach"
    }
  ],
  "Faxes": [
    {
      "Value": "et",
      "StrippedValue": "aut",
      "Description": "Integrated national intranet"
    },
    {
      "Value": "et",
      "StrippedValue": "aut",
      "Description": "Integrated national intranet"
    }
  ],
  "Description": "Enhanced systematic concept",
  "UpdatedBy": null,
  "CreatedBy": null,
  "Associate": null,
  "Business": null,
  "Category": null,
  "Country": null,
  "Persons": [
    {
      "Position": "aut",
      "PersonId": 678,
      "Mrmrs": "dolor",
      "Firstname": "Delmer",
      "Lastname": "Feil",
      "MiddleName": "Jacobs LLC",
      "Title": "alias",
      "Description": "Proactive analyzing hub",
      "Email": "selena@waters.info",
      "FullName": "Mrs. Marcellus August Aufderhar PhD",
      "DirectPhone": "635.673.9829 x9980",
      "FormalName": "O'Reilly Group",
      "CountryId": 788,
      "ContactId": 113,
      "ContactName": "Gottlieb Inc and Sons",
      "Retired": 734,
      "Rank": 612,
      "ActiveInterests": 210,
      "ContactDepartment": "",
      "ContactCountryId": 172,
      "ContactOrgNr": "810272",
      "FaxPhone": "029-387-0530",
      "MobilePhone": "(871)375-7868",
      "ContactPhone": "(819)173-3633",
      "AssociateName": "Larkin-Hodkiewicz",
      "AssociateId": 104,
      "UsePersonAddress": true,
      "ContactFax": "velit",
      "Kanafname": "aliquam",
      "Kanalname": "et",
      "Post1": "optio",
      "Post2": "omnis",
      "Post3": "voluptatem",
      "EmailName": "helena@spinka.info",
      "ContactFullName": "Dr. Litzy Greta Waelchi",
      "ActiveErpLinks": 858,
      "TicketPriorityId": 600,
      "SupportLanguageId": 783,
      "SupportAssociateId": 387,
      "CategoryName": "VIP Customer"
    }
  ],
  "NoMailing": true,
  "Kananame": "quaerat",
  "Xstop": true,
  "ActiveInterests": 545,
  "GroupId": 848,
  "ActiveStatusMonitorId": 921,
  "SupportAssociate": null,
  "TicketPriority": null,
  "CustomerLanguage": null,
  "Deleted": 455,
  "DbiAgentId": 310,
  "DbiLastSyncronized": "2004-07-10T12:15:26.7766379+02:00",
  "DbiKey": "quia",
  "DbiLastModified": "2003-02-24T12:15:26.7766379+01:00",
  "SupportPerson": null,
  "Address": null,
  "Source": 712,
  "ActiveErpLinks": 632,
  "BounceEmails": [
    "marcos_bins@schadendach.info",
    "glenda.schiller@beer.ca"
  ],
  "Domains": [
    "magnam",
    "rem"
  ],
  "UserDefinedFields": {
    "SuperOffice:1": "Prof. Thurman Leon Emard",
    "SuperOffice:2": "True"
  },
  "ExtraFields": {
    "ExtraFields1": "iste",
    "ExtraFields2": "ipsa"
  },
  "CustomFields": {
    "CustomFields1": "facere",
    "CustomFields2": "voluptatum"
  }
}
```

## Sample response

```http_
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{
  "1": "velit",
  "2": "consectetur"
}
```