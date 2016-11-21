---
title: "object (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "object_CSharpKeyword"
  - "object"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "object-Schlüsselwort [C#]"
ms.assetid: 93f60c0b-e17a-40a9-9362-cca5fb77b0e7
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# object (C#-Referenz)
Der `object`\-Typ ist ein Alias für <xref:System.Object> in .NET Framework.  Im vereinheitlichten Typsystem von C\# erben alle Typen \(vordefinierte und benutzerdefinierte Typen, Verweis\- und Werttypen\) direkt oder indirekt von <xref:System.Object>.  Den Variablen vom `object`\-Typ können Sie Werte eines beliebigen Typs zuweisen.  Wenn eine Variable eines Werttyps in ein Objekt konvertiert wird, wird sie als *geschachtelt* bezeichnet.  Wird eine Variable des Objekttyps in einen Werttyp konvertiert, wird sie als *nicht geschachtelt* bezeichnet.  Weitere Informationen finden Sie unter [Boxing und Unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Variablen vom `object`\-Typ Werte eines beliebigen Datentyps annehmen und wie Variablen vom `object`\-Typ Methoden für <xref:System.Object> aus .NET Framework verwenden können.  
  
 [!CODE [csrefKeywordsTypes#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#16)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Verweistypen](../../../csharp/language-reference/keywords/reference-types.md)   
 [Werttypen](../../../csharp/language-reference/keywords/value-types.md)