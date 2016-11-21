---
title: "XML CDATA Literal (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.XmlLiteralCdata"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "CDATA literal [Visual Basic]"
  - "XML CDATA literal [Visual Basic]"
  - "XML literals [Visual Basic], CDATA"
ms.assetid: 9eafb6a4-dd9d-4866-85e8-0654c65abc44
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML CDATA Literal (Visual Basic)
Ein Literal, das ein <xref:System.Xml.Linq.XCData>\-Objekt darstellt.  
  
## Syntax  
  
```  
<![CDATA[content]]>  
```  
  
## Teile  
 `<![CDATA[`  
 Erforderlich.  Kennzeichnet den Anfang des XML\-CDATA\-Abschnitts.  
  
 `content`  
 Erforderlich.  Textinhalt, der im XML\-CDATA\-Abschnitt enthalten sein soll.  
  
 `]]>`  
 Erforderlich.  Kennzeichnet das Ende des Abschnitts.  
  
## Rückgabewert  
 Ein <xref:System.Xml.Linq.XCData>\-Objekt.  
  
## Hinweise  
 XML\-CDATA\-Abschnitte enthalten unformatierten Text, der zum jeweiligen XML\-Code gehört, jedoch nicht analysiert wird.  Ein XML\-CDATA\-Abschnitt kann beliebigen Text enthalten.  Dazu gehören auch reservierte XML\-Zeichen.  Der XML\-CDATA\-Abschnitt endet mit der Sequenz "\]\]\>".  Dies impliziert folgende Punkte:  
  
-   In einem XML\-CDATA\-Literal können keine eingebetteten Ausdrücke verwendet werden, da die Trennzeichen für eingebettete Ausdrücke gültiger XML\-CDATA\-Inhalt sind.  
  
-   XML\-CDATA\-Abschnitte können nicht geschachtelt werden, da der `content` nicht den Wert "\]\]\>" enthalten darf.  
  
 Ein XML\-CDATA\-Literal kann einer Variablen zugewiesen oder in einem XML\-Elementliteral eingeschlossen werden.  
  
> [!NOTE]
>  Ein XML\-Literal kann mehrere Zeilen umfassen, verwendet jedoch keine Zeilenfortsetzungszeichen.  So kann Inhalt aus einem XML\-Dokument kopiert und direkt in ein [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Programm eingefügt werden.  
  
 Der [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler konvertiert das XML\-CDATA\-Literal in einen Aufruf des <xref:System.Xml.Linq.XCData.%23ctor%2A>\-Konstruktors.  
  
## Beispiel  
 Im folgenden Beispiel wird ein CDATA\-Abschnitt mit dem Text "Can contain literal \<XML\> Tags" erstellt.  
  
 [!CODE [VbXMLSamples#23](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#23)]  
  
## Siehe auch  
 <xref:System.Xml.Linq.XCData>   
 [XML Element Literal](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)   
 [XML Literals](../../../visual-basic/language-reference/xml-literals/index.md)   
 [Creating XML in Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)