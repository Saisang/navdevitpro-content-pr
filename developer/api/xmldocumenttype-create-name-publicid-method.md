---
title: "Create Method"
ms.author: SusanneWindfeldPedersen
ms.custom: na
ms.date: 30/06/2017
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2017"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 1
manager: edupont
author: SusanneWindfeldPedersen
---

# Create Method
Creates an XmlDocumentType node.  
```  
XmlDocumentType := XmlDocumentType.Create(Name, PublicId)  
```  
## Parameters
*Name*    
&emsp;Type: String  
A string that contains the qualified name of the DTD, which is the same as the qualified name of the root element of the XML document.  
  
*PublicId*    
&emsp;Type: String  
A string that contains the public identifier of an external public DTD.  
  
## Return Value
*XmlDocumentType*  
&emsp;Type: XmlDocumentType  
  
## See Also
[Getting Started](../devenv-get-started.md)  
[Developing Extensions Using the New Development Environment](../devenv-dev-overview.md)  