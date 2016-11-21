---
title: "Operator&#160;= (C#-Referenz) | Microsoft Docs"
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
  - "=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "= (Operator) [C#]"
ms.assetid: d802a6d5-32f0-42b8-b180-12f5a081bfc1
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;= (C#-Referenz)
Der Zuweisungsoperator \(`=`\) speichert den Wert seines rechtsseitigen Operanden an dem Speicherort, in der Eigenschaft oder in dem Indexer, der durch seinen linksseitigen Operanden angegeben wird, und gibt den Wert als Ergebnis zurück.  Die Operanden müssen demselben Typ angehören, oder der rechtsseitige Operand muss implizit in den Typ des linksseitigen Operanden konvertierbar sein.  
  
## Hinweise  
 Der Zuweisungsoperator kann nicht überladen werden.  Sie können jedoch implizite Konvertierungsoperatoren für einen Typ definieren, um den Zuweisungsoperator mit dem entsprechenden Typ zu verwenden.  Weitere Informationen finden Sie unter [Verwenden von Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).  
  
## Beispiel  
 [!CODE [csRefOperators#49](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#49)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)