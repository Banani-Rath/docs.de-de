---
title: "How to: Access XML Descendant Elements (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "XML descendent axis property [Visual Basic]"
  - "XML axis [Visual Basic], descendent"
  - "descendent axis property [Visual Basic]"
  - "XML [Visual Basic], accessing"
ms.assetid: aabfa258-4112-4e7e-bab9-403f96072ef7
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Access XML Descendant Elements (Visual Basic)
In diesem Beispiel wird gezeigt, wie mit einer untergeordneten Achseneigenschaft auf alle XML\-Elemente zugegriffen werden kann, die einen angegebenen Namen haben und einem XML\-Element untergeordnet sind.  Dabei wird mit der `Value`\-Eigenschaft der Wert des ersten Elements aus der Auflistung abgerufen, den die untergeordnete `name`\-Achseneigenschaft zurückgibt.  Die untergeordnete `name`\-Achseneigenschaft ruft alle Elemente mit dem Namen `name` ab, die im `contacts`\-Objekt enthalten sind.  In diesem Beispiel wird die untergeordnete `phone`\-Achseneigenschaft auch verwendet, um auf alle untergeordneten Elemente mit dem Namen `phone` zuzugreifen, die im `contacts`\-Objekt enthalten sind.  
  
## Beispiel  
 [!CODE [VbXMLSamples#31](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#31)]  
  
## Kompilieren des Codes  
 Dieses Beispiel setzt Folgendes voraus:  
  
-   Ein Verweis auf den <xref:System.Xml.Linq>\-Namespace.  
  
## Siehe auch  
 <xref:System.Xml.Linq.XContainer.Descendants%2A?displayProperty=fullName>   
 [XML Descendant Axis Property](../../../../visual-basic/language-reference/xml-axis/xml-descendant-axis-property.md)   
 [XML Value Property](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)   
 [Accessing XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)