---
title: "How to: Access XML Child Elements (Visual Basic) | Microsoft Docs"
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
  - "XML axis [Visual Basic], child"
  - "child axis property [Visual Basic]"
  - "XML child axis property [Visual Basic]"
  - "XML [Visual Basic], accessing"
ms.assetid: 6689eb36-c471-469f-a82d-099ab8197b25
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Access XML Child Elements (Visual Basic)
In diesem Beispiel ist dargestellt, wie eine untergeordnete Achseneigenschaft verwendet wird, um auf alle untergeordneten XML\-Elemente zuzugreifen, die einen festgelegten Namen in einem XML\-Element haben.  Insbesondere wird die Eigenschaft <xref:System.Xml.Linq.XElement.Value%2A> verwendet, um den Wert des ersten Elements in der Sammlung abzurufen, der von der untergeordneten Achseneigenschaft `name` zurückgegeben wird.  Von der untergeordneten Achseneigenschaft `name` werden alle untergeordneten Elemente mit dem Namen `phone` im `contact`\-Objekt abgerufen.  In diesem Beispiel wird die untergeordnete Achseneigenschaft `phone` außerdem verwendet, um auf alle untergeordneten Elemente mit dem Namen `phone` zuzugreifen, die im `contact`\-Objekt enthalten sind.  
  
## Beispiel  
 [!CODE [VbXMLSamples#10](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#10)]  
  
## Kompilieren des Codes  
 Dieses Beispiel setzt Folgendes voraus:  
  
-   Ein Verweis auf den <xref:System.Xml.Linq>\-Namespace.  
  
## Siehe auch  
 <xref:System.Xml.Linq.XContainer.Elements%2A?displayProperty=fullName>   
 [XML Child Axis Property](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)   
 [XML Value Property](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)   
 [Accessing XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)