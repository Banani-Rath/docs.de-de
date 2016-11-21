---
title: "Operator&#160;&gt; (C#-Referenz) | Microsoft Docs"
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
  - ">_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "> (Operator) [C#]"
  - "Größer als-Operator (>) [C#]"
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;&gt; (C#-Referenz)
Alle numerischen Typen und Enumerationstypen definieren einen relationalen Operator "größer als" \(`>`\), der `true` zurückgibt, wenn der erste Operand größer als der zweite ist. Andernfalls gibt er `false` zurück.  
  
## Hinweise  
 Benutzerdefinierte Typen können den Operator `>` überladen \(siehe [Operator](../../../csharp/language-reference/keywords/operator.md)\).  Wenn `>` überladen wird, muss auch [\<](../../../csharp/language-reference/operators/less-than-operator.md) überladen werden.  Beim Überladen eines binären Operators wird implizit auch der zugehörige Zuweisungsoperator überladen, falls vorhanden.  
  
## Beispiel  
 [!CODE [csRefOperators#29](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#29)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)   
 [Explizit](../../../csharp/language-reference/keywords/explicit.md)