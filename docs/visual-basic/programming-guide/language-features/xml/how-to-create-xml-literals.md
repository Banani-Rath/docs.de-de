---
title: "How to: Create XML Literals (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "XML literals [Visual Basic], creating"
ms.assetid: 573a6db5-b14d-4e42-b356-8cc7e2d77745
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create XML Literals (Visual Basic)
Mithilfe eines XML\-Literals können Sie ein XML\-Dokument, \-Fragment oder \-Element direkt im Code erstellen.  In den Beispielen in diesem Thema wird veranschaulicht, wie ein XML\-Element mit drei untergeordneten Elementen erstellt wird, und wie ein XML\-Dokument erstellt wird.  
  
 Sie können auch die [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-APIs verwenden, um [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekte zu erstellen.  Weitere Informationen finden Sie unter <xref:System.Xml.Linq.XElement>.  
  
### So erstellen Sie ein XML\-Element  
  
-   Erstellen Sie XML inline, indem Sie die XML\-Literalsyntax verwenden, die der tatsächlichen XML\-Syntax entspricht.  
  
     [!CODE [VbXMLSamples#5](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#5)]  
  
     Führen Sie den Code aus.  Ausgabe dieses Codes:  
  
     `<contact>`  
  
     `<name>Patrick Hines</name>`  
  
     `<phone type="home">206-555-0144</phone>`  
  
     `<phone type="work">425-555-0145</phone>`  
  
     `</contact>`  
  
### So erstellen Sie ein XML\-Dokument  
  
-   Erstellen Sie das XML\-Dokument inline.  Mit dem folgenden Code wird ein XML\-Dokument mit Literalsyntax, einer XML\-Deklaration, einer Verarbeitungsanweisung, einem Kommentar und einem Element, das ein anderes Element enthält, erstellt.  
  
     [!CODE [VbXMLSamples#30](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#30)]  
  
     Führen Sie den Code aus.  Ausgabe dieses Codes:  
  
     `<?xml-stylesheet type="text/xsl" href="show_book.xsl"?>`  
  
     `<!-- Tests that the application works.  -->`  
  
     `<books>`  
  
     `<book/>`  
  
     `</books>`  
  
## Siehe auch  
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)   
 [Creating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)   
 [XML Element Literal](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)   
 [XML Document Literal](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)