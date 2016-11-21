---
title: "Operator&#160;^= (C#-Referenz) | Microsoft Docs"
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
  - "^=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "^= (Operator) [C#]"
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;^= (C#-Referenz)
Der XOR\-Zuweisungsoperator.  
  
## Hinweise  
 Ein Ausdruck der Form  
  
```  
x ^= y  
```  
  
 wird ausgewertet als  
  
```  
x = x ^ y  
```  
  
 mit der Ausnahme, dass `x` nur einmal ausgewertet wird.  Der [Operator ^](../../../csharp/language-reference/operators/xor-operator.md) führt eine bitweise XOR\-Operation für ganzzahlige Operanden aus sowie logische XOR\-Operationen für [bool](../../../csharp/language-reference/keywords/bool.md)\-Operanden.  
  
 Der Operator ^\= kann nicht direkt überladen werden. Benutzerdefinierte Typen können jedoch den [^\-Operator](../../../csharp/language-reference/operators/xor-operator.md) \(siehe [Operator](../../../csharp/language-reference/keywords/operator.md)\) überladen.  
  
## Beispiel  
 [!CODE [csRefOperators#23](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#23)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)