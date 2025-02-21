---
title: Services87.SelectionAgent.EditContactSelectionMemberDetails SOAP
generated: 1
uid: Services87-Selection-EditContactSelectionMemberDetails
---

# Services87 Selection EditContactSelectionMemberDetails

SOAP request and response examples **Remote/Services87/Selection.svc**
Implemented by the <see cref="M:SuperOffice.Services87.ISelectionAgent.EditContactSelectionMemberDetails">SuperOffice.Services87.ISelectionAgent.EditContactSelectionMemberDetails</see> method.

## EditContactSelectionMemberDetails





[WSDL file for Services87/Selection](../Services87-Selection.md)

Obtain a ticket from the [Services87/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## EditContactSelectionMemberDetails Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Selection="http://www.superoffice.net/ws/crm/NetServer/Services87">
  <Selection:ApplicationToken>1234567-1234-9876</Selection:ApplicationToken>
  <Selection:Credentials>
    <Selection:Ticket>7T:1234abcxyzExample==</Selection:Ticket>
  </Selection:Credentials>
 <SOAP-ENV:Body>
   <Selection:EditContactSelectionMemberDetails>
    <Selection:SelectionId xsi:type="xsd:int">0</Selection:SelectionId>
    <Selection:SelectionMemberEditValues xsi:type="Selection:SelectionMemberEditValues">
     <Selection:CompanyCategory xsi:type="xsd:int">0</Selection:CompanyCategory>
     <Selection:CompanyBusiness xsi:type="xsd:int">0</Selection:CompanyBusiness>
     <Selection:CompanyOurContact xsi:type="xsd:int">0</Selection:CompanyOurContact>
     <Selection:CompanyName xsi:type="xsd:string"></Selection:CompanyName>
     <Selection:CompanyDepartment xsi:type="xsd:string"></Selection:CompanyDepartment>
     <Selection:CompanyNumber xsi:type="xsd:string"></Selection:CompanyNumber>
     <Selection:CompanyCode xsi:type="xsd:string"></Selection:CompanyCode>
     <Selection:ContactPosition xsi:type="xsd:int">0</Selection:ContactPosition>
     <Selection:ChangeCompanyCategory xsi:type="xsd:boolean">false</Selection:ChangeCompanyCategory>
     <Selection:ChangeCompanyBusiness xsi:type="xsd:boolean">false</Selection:ChangeCompanyBusiness>
     <Selection:ChangeCompanyOurContact xsi:type="xsd:boolean">false</Selection:ChangeCompanyOurContact>
     <Selection:ChangeCompanyName xsi:type="xsd:boolean">false</Selection:ChangeCompanyName>
     <Selection:ChangeCompanyDepartment xsi:type="xsd:boolean">false</Selection:ChangeCompanyDepartment>
     <Selection:ChangeCompanyNumber xsi:type="xsd:boolean">false</Selection:ChangeCompanyNumber>
     <Selection:ChangeCompanyCode xsi:type="xsd:boolean">false</Selection:ChangeCompanyCode>
     <Selection:ChangeContactPosition xsi:type="xsd:boolean">false</Selection:ChangeContactPosition>
     <Selection:CompanyCountry xsi:type="xsd:int">0</Selection:CompanyCountry>
     <Selection:ChangeCompanyCountry xsi:type="xsd:boolean">false</Selection:ChangeCompanyCountry>
     <Selection:ContactJobTitle xsi:type="xsd:string"></Selection:ContactJobTitle>
     <Selection:ChangeContactJobTitle xsi:type="xsd:boolean">false</Selection:ChangeContactJobTitle>
     <Selection:CompanyOrgNr xsi:type="xsd:string"></Selection:CompanyOrgNr>
     <Selection:ChangeCompanyOrgNr xsi:type="xsd:boolean">false</Selection:ChangeCompanyOrgNr>
    </Selection:SelectionMemberEditValues>
   </Selection:EditContactSelectionMemberDetails>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## EditContactSelectionMemberDetails Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices872="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices871="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Selection="http://www.superoffice.net/ws/crm/NetServer/Services87">
 <SOAP-ENV:Body>
  <Selection:EditContactSelectionMemberDetailsResponse>
  </Selection:EditContactSelectionMemberDetailsResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

