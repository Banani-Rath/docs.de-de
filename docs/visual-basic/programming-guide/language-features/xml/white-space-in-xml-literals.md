---
title: "White Space in XML Literals (Visual Basic) | Microsoft Docs"
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
  - "white space [XML in Visual Basic]"
  - "XML literals [Visual Basic], white space"
ms.assetid: dfe3a9ff-d69a-418e-a6b5-476f4ed84219
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# White Space in XML Literals (Visual Basic)
Der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler bindet nur die signifikanten Leerzeichen eines XML\-Literals ein, wenn er ein [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekt erstellt.  Die nicht signifikanten Leerzeichen werden nicht übernommen.  
  
## Signifikante und nicht signifikante Leerzeichen  
 Leerzeichen in XML\-Literalen sind nur in drei Bereichen signifikant:  
  
-   Wenn sie sich in einem Attributwert befinden.  
  
-   Wenn sie Teil des Textinhalts eines Elements sind und der Text auch andere Zeichen enthält.  
  
-   Wenn sie sich in einem eingebetteten Ausdruck des Textinhalts eines Elements befinden.  
  
 Andernfalls behandelt der Compiler Leerzeichen als nicht signifikant und schließt sie nicht in das [!INCLUDE[sqltecxlinq](../../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)]\-Objekt für das Literal ein.  
  
 Zum Einschließen von nicht signifikanten Leerzeichen in ein XML\-Literal wird ein eingebetteter Ausdruck verwendet, der ein Zeichenfolgenliteral mit den Leerzeichen beinhaltet.  
  
> [!NOTE]
>  Wenn das `xml:space`\-Attribut in einem XML\-Elementliteral vorhanden ist, schließt der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler das Attribut im <xref:System.Xml.Linq.XElement>\-Objekt ein. Jedoch ändert das Hinzufügen dieses Attributs nicht die Behandlung von Leerzeichen durch den Compiler.  
  
## Beispiele  
 Das folgende Beispiel enthält zwei XML\-Elemente, ein äußeres und ein inneres.  Beide Elemente enthalten Leerzeichen im Textinhalt.  Die Leerzeichen im äußeren Element sind nicht signifikant, weil das Element nur Leerzeichen und ein XML\-Element enthält.  Die Leerzeichen im inneren Element sind signifikant, da das Element Leerzeichen und Text enthält.  
  
 [!CODE [VbXMLSamples#29](../CodeSnippet/VS_Snippets_VBCSharp/VbXMLSamples#29)]  
  
 Beim Ausführen zeigt dieser Code den folgenden Text an.  
  
```  
<outer>  
  <inner>  
                                          Inner text  
                                      </inner>  
</outer>  
```  
  
## Siehe auch  
 [Creating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)