---
title: "implicit (C#-Referenz) | Microsoft Docs"
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
  - "implicit"
  - "implicit_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "implicit-Schlüsselwort [C#]"
ms.assetid: 34db590e-eb3a-4f11-88d0-ffb3cd753dab
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# implicit (C#-Referenz)
Das `implicit`\-Schlüsselwort wird verwendet, um einen impliziten benutzerdefinierten Typkonvertierungsoperator zu deklarieren.  Wenn durch die Konvertierung kein Datenverlust zu befürchten ist, können Sie es verwenden, um implizite Konvertierungen zwischen einem benutzerdefinierten Typ und einem anderen Typ zu ermöglichen.  
  
## Beispiel  
 [!CODE [csrefKeywordsConversion#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#5)]  
  
 Durch implizite Konvertierungen kann die Lesbarkeit des Quellcodes verbessert werden, da nicht erforderliche Typumwandlungen entfernt werden.  Da implizite Konvertierungen jedoch keine explizite Umwandlung von einem Typ in einen anderen erfordern, ist Vorsicht angebracht, um unerwartete Ergebnisse zu vermeiden.  In der Regel sollten durch implizite Konvertierungsoperatoren keine Ausnahmen ausgelöst werden oder Informationen verloren gehen, sodass sie sicher verwendet werden können, ohne dass sich der Programmierer dessen bewusst ist.  Ein Konvertierungsoperator, der diese Kriterien nicht erfüllen kann, sollte als `explicit` markiert werden.  Weitere Informationen hierzu finden Sie unter [Verwenden von Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Explizit](../../../csharp/language-reference/keywords/explicit.md)   
 [Operator](../../../csharp/language-reference/keywords/operator.md)   
 [Gewusst wie: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)