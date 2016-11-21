---
title: "How to: Determine the String Associated with an Enumeration Value (Visual Basic) | Microsoft Docs"
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
  - "enumerations [Visual Basic]"
  - "strings [Visual Basic], enumeration values"
  - "values, enumeration members"
ms.assetid: 9253e7c8-579c-49a2-8f26-392b20ea99eb
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Determine the String Associated with an Enumeration Value (Visual Basic)
Mit der <xref:System.Enum.GetValues%2A>\-Methode und der <xref:System.Enum.GetNames%2A>\-Methode können Sie die Zeichenfolgen und Werte ermitteln, die Enumerationsmembern zugeordnet sind.  
  
### So bestimmen Sie die einer Enumeration zugeordnete Zeichenfolge  
  
-   Rufen Sie mit der <xref:System.Enum.GetNames%2A>\-Methode die den Enumerationsmembern zugeordneten Zeichenfolgen ab.  In diesem Beispiel wird eine Enumeration, `flavorEnum`, deklariert. Anschließend werden mithilfe der <xref:System.Enum.GetNames%2A>\-Methode die Zeichenfolgen angezeigt, die den einzelnen Membern zugeordnet sind.  
  
     [!CODE [VbEnumsTask#2](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#2)]  
  
## Siehe auch  
 <xref:System.Enum.GetValues%2A>   
 <xref:System.Enum.GetNames%2A>   
 <xref:System.Enum>   
 [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)   
 [How to: Refer to an Enumeration Member](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)   
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [How to: Iterate Through An Enumeration in Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)   
 [When to Use an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)   
 [Enum Statement](../../../../visual-basic/language-reference/statements/enum-statement.md)