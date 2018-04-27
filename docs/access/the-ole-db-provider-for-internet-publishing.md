---
title: "The OLE DB Provider for Internet Publishing"
 
 
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
  
localization_priority: Normal
ms.assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
description: "The ADO Record and Stream objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage. With ADO, you can specify the source of a Record , Stream , or Recordset to be a URL. You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties."
---

# The OLE DB Provider for Internet Publishing

The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage. With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL. You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties. 
  
For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).
  
The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.
  
There are three ways to connect ADO to the Internet Publishing Provider:
  
- Specify "URL=" in the connection string. For example:
    
  ```
   
  objConn.Open "URL=http://servername" 
  
  ```

- Specify Msdaipp.dso for the  *Provider*  keyword of the connection string. For example: 
    
  ```
   
  objConn.Open "provider=MSDAIPP.DSO;data source=http://servername" 
  
  ```

- Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example: 
    
  ```
   
  objConn.Provider = "MSDAIPP.DSO" 
  objConn.Open "http://servername" 
  
  ```

> [!NOTE]
> If Msdaipp.dso is explicitly specified as the value of the provider, either with the  *Provider*  connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string. If you do, an error will occur. Instead, simply specify the URL as shown above. 
  
For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.
  
