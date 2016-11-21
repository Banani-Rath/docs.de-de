---
title: "XML Literals Overview (Visual Basic) | Microsoft Docs"
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
  - "XML literals [Visual Basic], about XML literals"
  - "declaring XML literals [Visual Basic]"
  - "LINQ to XML [Visual Basic], XML literals"
  - "literals [Visual Basic], XML"
ms.assetid: 37987c15-4ab8-471b-bd45-399816bfb57f
caps.latest.revision: 27
caps.handback.revision: 27
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML Literals Overview (Visual Basic)
Mit einem *XML\-Literal* kann XML direkt in den [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Code integriert werden. Die XML\-Literalsyntax stellt [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekte dar und ähnelt der XML 1.0\-Syntax. Dies vereinfacht die programmgesteuerte Erstellung von XML\-Elementen und \-Dokumenten, da der Code dieselbe Struktur hat wie der fertige XML\-Code.  
  
 [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] kompiliert XML\-Literale in [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekte.  [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)] stellt ein einfaches Objektmodell zur Erstellung und Bearbeitung von XML zur Verfügung, das gut in [!INCLUDE[vbteclinqext](../../../../csharp/getting-started/includes/vbteclinqext_md.md)] integriert ist.  Weitere Informationen finden Sie unter <xref:System.Xml.Linq.XElement>.  
  
 Sie können einen [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Ausdruck in ein XML\-Literal einbetten.  Zur Laufzeit erstellt die Anwendung ein [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekt für jedes Literal. Dieses beinhaltet die Werte der eingebetteten Ausdrücke.  Damit kann dynamischer Inhalt in einem XML\-Literal angegeben werden.  Weitere Informationen finden Sie unter [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
 Weitere Informationen über die Unterschiede zwischen XML\-Literalsyntax und XML 1.0\-Syntax finden Sie unter [XML Literals and the XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md).  
  
## Einfache Literale  
 Sie können ein [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekt in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Code erstellen, indem Sie gültigen XML\-Code eingeben oder einfügen.  Ein XML\-Elementliteral gibt ein <xref:System.Xml.Linq.XElement>\-Objekt zurück.  Weitere Informationen finden Sie unter [XML Element Literal](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md) und unter [XML Literals and the XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md).  Im folgenden Beispiel wird ein XML\-Element mit mehreren untergeordneten Elementen erstellt.  
  
 [!CODE [VbXMLSamples#5](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#5)]  
  
 Ein XML\-Dokument kann erstellt werden, indem einem XML\-Literal `<?xml version="1.0"?>` vorangestellt wird, wie im folgenden Beispiel gezeigt wird.  Ein XML\-Dokumentliteral gibt ein <xref:System.Xml.Linq.XDocument>\-Objekt zurück.  Weitere Informationen finden Sie unter [XML Document Literal](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md).  
  
 [!CODE [VbXMLSamples#6](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#6)]  
  
> [!NOTE]
>  Die XML\-Literalsyntax in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] ist nicht identisch mit der Syntax der XML 1.0\-Spezifikation.  Weitere Informationen finden Sie unter [XML Literals and the XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md).  
  
## Zeilenfortsetzung  
 Ein XML\-Literal kann mehrere Zeilen umfassen, ohne dass Zeilenfortsetzungszeichen \(die Leerzeichen\-Unterstrich\-EINGABETASTE\-Sequenz\) verwendet werden.  Dies vereinfacht den Vergleich von XML\-Literalen im Code mit XML\-Dokumenten.  
  
 Der Compiler behandelt Zeilenfortsetzungszeichen als Teil eines XML\-Literals.  Deshalb sollte die Leerzeichen\-Unterstrich\-EINGABETASTE\-Sequenz nur verwendet werden, wenn sie Teil des [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekts ist.  
  
 Zeilenfortsetzungszeichen werden jedoch benötigt, wenn ein mehrzeiliger Ausdruck in einem eingebetteten Ausdruck vorliegt.  Weitere Informationen finden Sie unter [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
## Einbetten von Abfragen in XML\-Literalen  
 In einem eingebetteten Ausdruck kann eine Abfrage verwendet werden.  In diesem Fall werden die von der Abfrage zurückgegebenen Elemente dem XML\-Element hinzugefügt.  Damit kann dynamischer Inhalt, wie beispielsweise das Ergebnis der Abfrage eines Benutzers, einem XML\-Literal hinzugefügt werden.  
  
 Im folgenden Code wird zum Beispiel eine eingebettete Abfrage verwendet, um XML\-Elemente aus den Membern des `phoneNumbers2`\-Arrays zu erstellen und diese als untergeordnete Elemente von `contact2` hinzuzufügen.  
  
 [!CODE [VbXMLSamples#7](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#7)]  
  
## So erzeugt der Compiler Objekte aus XML\-Literalen  
 Der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler übersetzt XML\-Literale in Aufrufe der entsprechenden [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Konstruktoren, um das [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekt zu erstellen.  Das folgende Codebeispiel wird vom [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler beispielsweise in einen Aufruf des <xref:System.Xml.Linq.XProcessingInstruction>\-Konstruktors für die XML\-Versionsanweisung, in Aufrufe des <xref:System.Xml.Linq.XElement>\-Konstruktors für die Elemente `<contact>`, `<name>` und `<phone>` und in Aufrufe des <xref:System.Xml.Linq.XAttribute>\-Konstruktors für das `type`\-Attribut übersetzt.  Genauer gesagt, ruft der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler für die Attribute des folgenden Beispiels den <xref:System.Xml.Linq.XAttribute.%23ctor%28System.Xml.Linq.XName%2CSystem.Object%29>\-Konstruktor zweimal auf.  Der erste Aufruf übergibt den Wert `type` für den `name`\-Parameter und den Wert `home` für den `value`\-Parameter.  Der zweite Aufruf übergibt ebenfalls den Wert `type` für den `name`\-Parameter, jedoch den Wert `work` für den `value`\-Parameter.  
  
 [!CODE [VbXMLSamples#6](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#6)]  
  
## Siehe auch  
 <xref:System.Xml.Linq.XElement>   
 [Creating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)   
 [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)   
 [XML Document Literal](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)   
 [XML Element Literal](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)   
 [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md)