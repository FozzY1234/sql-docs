---
title: "Subscribe Element (XMLA) | Microsoft Docs"
ms.custom: ""
ms.date: "06/13/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.technology: 
  - "analysis-services"
  - "docset-sql-devref"
ms.topic: "reference"
api_name: 
  - "Subscribe Element"
api_location: 
  - "http://schemas.microsoft.com/analysisservices/2003/engine"
topic_type: 
  - "apiref"
f1_keywords: 
  - "urn:schemas-microsoft-com:xml-analysis#Subscribe"
  - "microsoft.xml.analysis.subscribe"
  - "http://schemas.microsoft.com/analysisservices/2003/engine#Subscribe"
helpviewer_keywords: 
  - "Subscribe command"
ms.assetid: aad50dd7-44d4-4d83-a973-187f9aed35ec
author: minewiskan
ms.author: owend
manager: craigg
---
# Subscribe Element (XMLA)
  Subscribes to a trace and returns a rowset that contains the trace events from a [!INCLUDE[msCoName](../../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)] instance.  
  
## Syntax  
  
```xml  
  
<Command>  
   <Subscribe>  
      <Object>...</Object>  
   </Subscribe>  
</Command>  
```  
  
## Element Characteristics  
  
|Characteristic|Description|  
|--------------------|-----------------|  
|Data type and length|None|  
|Default value|None|  
|Cardinality|0-n: Optional element that can occur more than once.|  
  
## Element Relationships  
  
|Relationship|Element|  
|------------------|-------------|  
|Parent elements|[Command](../xml-elements-properties/command-element-xmla.md)|  
|Child elements|[Object](../xml-elements-properties/object-element-xmla.md)|  
  
## Remarks  
 The `Subscribe` command subscribes to and streams back a rowset from a specified trace on an [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)] instance. If an object other than a trace is specified in the `Object` element, an error occurs.  
  
 If the `Object` element is not specified, a session trace is defined and subscribed to on the [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)] instance. The session trace returns a fixed set of trace events from the current session.  
  
 The rowset stream returned by this command is terminated if the client application closes the connection to the [!INCLUDE[ssASnoversion](../../../includes/ssasnoversion-md.md)] instance, or if the session on which the `Subscribe` command is executed is terminated.  
  
## See Also  
 [Commands &#40;XMLA&#41;](xml-elements-commands.md)  
  
  
