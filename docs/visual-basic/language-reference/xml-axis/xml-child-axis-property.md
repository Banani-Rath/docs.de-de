---
title: "XML Child Axis Property (Visual Basic) | Microsoft Docs"
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
  - "vb.XmlPropertyChildAxis"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Visual Basic code, accessing XML"
  - "XML axis [Visual Basic], child"
  - "child axis property [Visual Basic]"
  - "XML child axis property [Visual Basic]"
  - "XML [Visual Basic], accessing"
ms.assetid: 89a59d00-985e-4f5c-b59f-29b47bad11cb
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML Child Axis Property (Visual Basic)
Bietet Zugriff auf die untergeordneten Elemente eines <xref:System.Xml.Linq.XElement>\-Objekts, eines <xref:System.Xml.Linq.XDocument>\-Objekts, einer Auflistung von <xref:System.Xml.Linq.XElement>\-Objekten oder einer Auflistung von <xref:System.Xml.Linq.XDocument>\-Objekten.  
  
## Syntax  
  
```  
  
object.<child>  
```  
  
## Teile  
  
|||  
|-|-|  
|Begriff|Definition|  
|`object`|Erforderlich.  Ein <xref:System.Xml.Linq.XElement>Objekt, ein <xref:System.Xml.Linq.XDocument>\-Objekt, eine Auflistung von <xref:System.Xml.Linq.XElement>Objekten oder eine Auflistung von <xref:System.Xml.Linq.XDocument>\-Objekten.|  
|.\<|Erforderlich.  Gibt den Anfang einer untergeordneten Achseneigenschaft an.|  
|`child`|Erforderlich.  Name der untergeordneten Knoten, auf die zugegriffen werden soll, in der Form \[`prefix``:`\]`name`.<br /><br /> -   `Prefix` – Optional.   XML\-Namespacepräfix für den untergeordneten Knoten.  Muss ein globaler XML\-Namespace sein, der mit einer `Imports`\-Anweisung definiert ist.<br />-   `Name` – Erforderlich.  Lokaler Name des untergeordneten Knotens.  Weitere Informationen finden Sie unter [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).|  
|\>|Erforderlich.  Gibt das Ende einer untergeordneten Achseneigenschaft an.|  
  
## Rückgabewert  
 Eine Auflistung von <xref:System.Xml.Linq.XElement>\-Objekten.  
  
## Hinweise  
 Sie können eine untergeordnete XML\-Achseneigenschaft verwenden, um auf untergeordnete Knoten eines <xref:System.Xml.Linq.XElement>\-Objekts oder eines <xref:System.Xml.Linq.XDocument>\-Objekts bzw. einer Auflistung von <xref:System.Xml.Linq.XElement>\-Objekten oder <xref:System.Xml.Linq.XDocument>\-Objekten über den Namen zuzugreifen.  Verwenden Sie die XML\-`Value`\-Eigenschaft, um auf den Wert des ersten untergeordneten Knotens in der zurückgegebenen Auflistung zuzugreifen.  Weitere Informationen finden Sie unter [XML Value Property](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).  
  
 Der [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler konvertiert die untergeordneten Achseneigenschaften in Aufrufe an die <xref:System.Xml.Linq.XContainer.Elements%2A>\-Methode.  
  
## XML\-Namespaces  
 Für den Namen in einer untergeordneten Achseneigenschaft können nur XML\-Namespacepräfixe verwendet werden, die mit der `Imports`\-Anweisung global deklariert wurden.  Es können keine XML\-Namespacepräfixe verwendet werden, die lokal innerhalb von XML\-Elementliteralen deklariert wurden.  Weitere Informationen finden Sie unter [Imports Statement \(XML Namespace\)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie auf die untergeordneten Knoten mit dem Namen `phone` aus dem `contact`\-Objekt zugegriffen werden kann.  
  
 [!CODE [VbXMLSamples#17](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#17)]  
  
 Durch diesen Code wird folgender Text angezeigt:  
  
 `Home Phone = 206-555-0144`  
  
## Beispiel  
 Im folgenden Beispiel wird dargestellt, wie auf die untergeordneten Knoten mit dem Namen `phone` aus der Auflistung zugegriffen werden kann, die von der untergeordneten `contact`\-Achseneigenschaft des `contacts`\-Objekts zurückgegeben wurde.  
  
 [!CODE [VbXMLSamples#18](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#18)]  
  
 Durch diesen Code wird folgender Text angezeigt:  
  
 `Home Phone = 206-555-0144`  
  
## Beispiel  
 Das folgende Beispiel deklariert `ns` als ein XML\-Namespacepräfix.  Anschließend wird mit dem Namespacepräfix ein XML\-Literal erstellt und auf den ersten untergeordneten Knoten mit dem qualifizierten Namen `ns:name` zugegriffen.  
  
 [!CODE [VbXMLSamples#19](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#19)]  
  
 Durch diesen Code wird folgender Text angezeigt:  
  
 `Patrick Hines`  
  
## Siehe auch  
 <xref:System.Xml.Linq.XElement>   
 [XML Axis Properties](../../../visual-basic/language-reference/xml-axis/xml-axis-properties.md)   
 [XML Literals](../../../visual-basic/language-reference/xml-literals/index.md)   
 [Creating XML in Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)   
 [Names of Declared XML Elements and Attributes](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)