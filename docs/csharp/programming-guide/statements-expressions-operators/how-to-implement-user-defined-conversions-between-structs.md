---
title: "Gewusst wie: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Benutzerdefinierte Konvertierungen [C#]"
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen (C#-Programmierhandbuch)
In diesem Beispiel werden die beiden Strukturen `RomanNumeral` und `BinaryNumeral` definiert, und es werden die Konvertierungen zwischen diesen Strukturen veranschaulicht.  
  
## Beispiel  
 [!CODE [csProgGuideStatements#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#13)]  
  
## Robuste Programmierung  
  
-   Im vorherigen Beispiel wird durch die Anweisung  
  
     [!CODE [csProgGuideStatements#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#14)]  
  
     eine Konvertierung von `RomanNumeral` in `BinaryNumeral` durchgeführt.  Da es keine direkte Konvertierung von `RomanNumeral` in `BinaryNumeral` gibt, wird `RomanNumeral` mithilfe einer Typumwandlung in einen `int`\-Typ konvertiert und mit einer weiteren Typumwandlung von `int` in `BinaryNumeral` konvertiert.  
  
-   Auch durch die Anweisung  
  
     [!CODE [csProgGuideStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#15)]  
  
     wird eine Konvertierung von `BinaryNumeral` in `RomanNumeral` durchgeführt.  Da durch `RomanNumeral` eine implizite Konvertierung von `BinaryNumeral` definiert wird, ist keine Typumwandlung erforderlich.  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)