---
uid: rejectreason
title: rejectreason
keywords:
  - "mdo"
  - "provider"
  - "mdo provider"
  - "rejectreason"
so.generated: true
so.date: 01.23.2023
so.topic: reference
so.envir:
  - "onsite"
  - "online"
---

# "rejectreason" MDO List
GenericMDOProvider reads MDO lists with default settings



Implemented by the <see cref="T:SuperOffice.CRM.Lists.GenericMDOProvider">GenericMDOProvider</see> class.
The name of the MDO list is 'rejectreason'.




## Sample Request

```http!
GET /api/v1/MDOList/rejectreason
Authorization: Basic dGplMDpUamUw
Accept: application/json; charset=utf-8
Accept-Language: *

```

## Sample Code
```cs
var listProvider = SuperOffice.CRM.Lists.SoListProviderFactory.Create("rejectreason", forceFlatList: true);
foreach (var item in listProvider.RootItems) {
    Console.WriteLine("{0} {1} {2} {3}", 
         item.Id, ResourceManager.ParseInlineResources(item.Name), item.StyleHint, item.ExtraInfo);
}
```

## Sample Output

|Id   | Name  |StyleHint|ExtraInfo |
| --- | ----- | ------- | -------- |
| 2 | Example | | |


## Related MDO Lists

* "rejectreasonheadings"
* "rejectreasonheadingswithallitem"
* "rejectreasonheadingswithallitemwithnoselection"
* "rejectreasonheadingswithnoselection"
* "rejectreasonwithallitem"
* "rejectreasonwithallitemwithnoselection"
* "rejectreasonwithnoselection"
