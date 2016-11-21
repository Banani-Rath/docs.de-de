---
title: "Operator&#160;| (C#-Referenz) | Microsoft Docs"
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
  - "|_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "| (Operator) [C#]"
  - "Binärer Operator (|) [C#]"
  - "Bitweiser OR-Operator [C#]"
ms.assetid: 82d6bb78-54c8-40bf-b679-531180ddaf70
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;| (C#-Referenz)
Binär        `|`  Operatoren sind für Ganzzahltypen und `bool` vordefiniert.  Für Ganzzahltypen  `|`berechnet das bitweise OR seiner Operanden.  Für `bool`\-Operanden berechnet der Operator  `|` das logische OR seiner Operanden. Dies bedeutet, dass das Ergebnis nur `false` ist, wenn beide Operanden `false` sind.  
  
## Hinweise  
 Benutzerdefinierte Typen können den Operator          `|` überladen \(siehe [Operator](../../../csharp/language-reference/keywords/operator.md)\).  
  
## Beispiel  
 [!CODE [csRefOperators#31](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#31)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)