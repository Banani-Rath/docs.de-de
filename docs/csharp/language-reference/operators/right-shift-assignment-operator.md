---
title: "Operator &gt;&gt;= (C#-Referenz) | Microsoft Docs"
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
  - ">>=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - ">>=-Operator (Rechtsschiebezuweisung) [C#]"
  - "Rechtsschiebezuweisungsoperator (>>=) [C#]"
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator &gt;&gt;= (C#-Referenz)
Der Rechtsschiebezuweisungsoperator.  
  
## Hinweise  
 Ein Ausdruck der Form  
  
```  
x >>= y  
```  
  
 wird ausgewertet als  
  
```  
x = x >> y  
```  
  
 mit der Ausnahme, dass `x` nur einmal ausgewertet wird.  Der [Operator \>\>](../../../csharp/language-reference/operators/right-shift-operator.md) verschiebt `x` um einen durch `y` angegebenen Betrag nach rechts.  
  
 Der Operator \>\>\= kann nicht direkt überladen werden, benutzerdefinierte Typen können jedoch den [Operator \>\>](../../../csharp/language-reference/operators/right-shift-operator.md) überladen \(siehe [Operator](../../../csharp/language-reference/keywords/operator.md)\).  
  
## Beispiel  
 [!CODE [csRefOperators#11](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#11)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)