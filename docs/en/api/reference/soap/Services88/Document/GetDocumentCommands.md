---
title: Services88.DocumentAgent.GetDocumentCommands SOAP
generated: 1
uid: Services88-Document-GetDocumentCommands
---

# Services88 Document GetDocumentCommands

SOAP request and response examples **Remote/Services88/Document.svc**
Implemented by the <see cref="M:SuperOffice.Services88.IDocumentAgent.GetDocumentCommands">SuperOffice.Services88.IDocumentAgent.GetDocumentCommands</see> method.

## GetDocumentCommands





[WSDL file for Services88/Document](../Services88-Document.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## GetDocumentCommands Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Document="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <Document:ApplicationToken>1234567-1234-9876</Document:ApplicationToken>
  <Document:Credentials>
    <Document:Ticket>7T:1234abcxyzExample==</Document:Ticket>
  </Document:Credentials>
 <SOAP-ENV:Body>
   <Document:GetDocumentCommands>
    <Document:DocumentId xsi:type="xsd:int">0</Document:DocumentId>
    <Document:AllowedReturnTypes xsi:type="NetServerServices882:ArrayOfstring">
     <NetServerServices882:string xsi:type="xsd:string"></NetServerServices882:string>
    </Document:AllowedReturnTypes>
   </Document:GetDocumentCommands>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## GetDocumentCommands Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:Document="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <Document:GetDocumentCommandsResponse>
   <Document:Response xsi:type="Document:ArrayOfCommandInfo">
    <Document:CommandInfo xsi:type="Document:CommandInfo">
     <Document:Name xsi:type="xsd:string"></Document:Name>
     <Document:DisplayName xsi:type="xsd:string"></Document:DisplayName>
     <Document:DisplayTooltip xsi:type="xsd:string"></Document:DisplayTooltip>
     <Document:IconHint xsi:type="xsd:string"></Document:IconHint>
     <Document:ReturnType xsi:type="Document:ReturnType">None</Document:ReturnType>
    </Document:CommandInfo>
   </Document:Response>
  </Document:GetDocumentCommandsResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

