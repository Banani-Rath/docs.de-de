---
title: "How to: Load XML from a File, String, or Stream (Visual Basic) | Microsoft Docs"
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
  - "XML [Visual Basic], loading"
  - "LINQ to XML [Visual Basic], loading XML from files"
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Load XML from a File, String, or Stream (Visual Basic)
Sie können [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md) erstellen und sie mit dem Inhalt aus einer externen Quelle wie beispielsweise einer Datei, einer Zeichenfolge oder einem Stream unter Verwendung von unterschiedlichen Methoden auffüllen.  Diese Methoden sind in den folgenden Beispielen dargestellt.  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So laden Sie XML aus einer Datei  
  
-   Um ein XML\-Literal wie beispielsweise ein <xref:System.Xml.Linq.XElement>\-Objekt oder ein <xref:System.Xml.Linq.XDocument>\-Objekt aus einer Datei aufzufüllen, verwenden Sie die `Load`\-Methode.  Diese Methode kann einen Dateipfad, einen Textstream oder einen XML\-Stream als Eingabe verwenden.  
  
     Im folgenden Codebeispiel ist dargestellt, wie mithilfe der <xref:System.Xml.Linq.XDocument.Load%28System.String%29>\-Methode ein <xref:System.Xml.Linq.XDocument>\-Objekt mit XML aus einer Textdatei aufgefüllt wird.  
  
     [!CODE [VbXMLSamples#43](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#43)]  
  
### So laden Sie XML aus einer Zeichenfolge  
  
-   Um ein XML\-Literal wie beispielsweise ein <xref:System.Xml.Linq.XElement>\-Objekt oder ein <xref:System.Xml.Linq.XDocument>\-Objekt aus einer Zeichenfolge aufzufüllen, verwenden Sie die `Parse`\-Methode.  
  
     Im folgenden Codebeispiel ist dargestellt, wie mithilfe der <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName>\-Methode ein <xref:System.Xml.Linq.XDocument>\-Objekt mit XML aus einer Zeichenfolge aufgefüllt wird.  
  
     [!CODE [VbXMLSamples#47](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#47)]  
  
### So laden Sie XML aus einem Stream  
  
-   Um ein XML\-Literal wie beispielsweise ein <xref:System.Xml.Linq.XElement>\-Objekt oder ein <xref:System.Xml.Linq.XDocument>\-Objekt aus einem Stream aufzufüllen, verwenden Sie die `Load`\-Methode oder die <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>\-Methode.  
  
 Im folgenden Codebeispiel ist dargestellt, wie mithilfe der <xref:System.Xml.Linq.XNode.ReadFrom%2A>\-Methode ein <xref:System.Xml.Linq.XDocument>\-Objekt mit XML aus einem XML\-Stream aufgefüllt wird.  
  
 [!CODE [VbXMLSamples#46](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#46)]  
  
## Siehe auch  
 <xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName>   
 <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>   
 [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md)   
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)   
 [Manipulating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)