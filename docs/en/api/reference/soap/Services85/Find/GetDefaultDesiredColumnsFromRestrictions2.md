---
title: Services85.FindAgent.GetDefaultDesiredColumnsFromRestrictions2 SOAP
generated: 1
uid: Services85-Find-GetDefaultDesiredColumnsFromRestrictions2
---

# Services85 Find GetDefaultDesiredColumnsFromRestrictions2

SOAP request and response examples **Remote/Services85/Find.svc**
Implemented by the <see cref="M:SuperOffice.Services85.IFindAgent.GetDefaultDesiredColumnsFromRestrictions2">SuperOffice.Services85.IFindAgent.GetDefaultDesiredColumnsFromRestrictions2</see> method.

## GetDefaultDesiredColumnsFromRestrictions2





[WSDL file for Services85/Find](../Services85-Find.md)

Obtain a ticket from the [Services85/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetDefaultDesiredColumnsFromRestrictions2 Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Find="http://www.superoffice.net/ws/crm/NetServer/Services85">
  <Find:ApplicationToken>1234567-1234-9876</Find:ApplicationToken>
  <Find:Credentials>
    <Find:Ticket>7T:1234abcxyzExample==</Find:Ticket>
  </Find:Credentials>
 <SOAP-ENV:Body>
   <Find:GetDefaultDesiredColumnsFromRestrictions2>
    <Find:ProviderName xsi:type="xsd:string"></Find:ProviderName>
    <Find:Restrictions xsi:type="xsd:string"></Find:Restrictions>
   </Find:GetDefaultDesiredColumnsFromRestrictions2>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetDefaultDesiredColumnsFromRestrictions2 Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices852="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices851="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Find="http://www.superoffice.net/ws/crm/NetServer/Services85">
 <SOAP-ENV:Body>
  <Find:GetDefaultDesiredColumnsFromRestrictions2Response>
   <Find:Response xsi:type="Find:ArrayOfArchiveColumnInfo">
    <Find:ArchiveColumnInfo xsi:type="Find:ArchiveColumnInfo">
     <Find:DisplayName xsi:type="xsd:string"></Find:DisplayName>
     <Find:DisplayTooltip xsi:type="xsd:string"></Find:DisplayTooltip>
     <Find:DisplayType xsi:type="xsd:string"></Find:DisplayType>
     <Find:CanOrderBy xsi:type="xsd:boolean">false</Find:CanOrderBy>
     <Find:Name xsi:type="xsd:string"></Find:Name>
     <Find:CanRestrictBy xsi:type="xsd:boolean">false</Find:CanRestrictBy>
     <Find:RestrictionType xsi:type="xsd:string"></Find:RestrictionType>
     <Find:RestrictionListName xsi:type="xsd:string"></Find:RestrictionListName>
     <Find:IsVisible xsi:type="xsd:boolean">false</Find:IsVisible>
     <Find:Width xsi:type="xsd:string"></Find:Width>
     <Find:IconHint xsi:type="xsd:string"></Find:IconHint>
     <Find:HeadingIconHint xsi:type="xsd:string"></Find:HeadingIconHint>
    </Find:ArchiveColumnInfo>
   </Find:Response>
  </Find:GetDefaultDesiredColumnsFromRestrictions2Response>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

