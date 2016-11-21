---
title: "Operator&#160;!= (C#-Referenz) | Microsoft Docs"
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
  - "!=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "!= (Operator) [C#]"
  - "Ungleichheitsoperator (!=) [C#]"
  - "Nicht gleich-Operator (!=) [C#]"
ms.assetid: eeff7a4e-ad6f-462d-9f8d-49e9b91c6c97
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;!= (C#-Referenz)
Der Ungleichheitsoperator \(`!=`\) gibt false zurück, wenn seine Operanden gleich sind, andernfalls gibt er true zurück.  Ungleichheitsoperatoren sind für alle Typen vordefiniert, einschließlich string und object.  Benutzerdefinierte Typen können den Operator `!=` überladen.  
  
## Hinweise  
 Für vordefinierte Werttypen gibt der Ungleichheitsoperator \(`!=`\) den Wert true zurück, wenn seine Operanden verschieden sind. Andernfalls gibt er false zurück.  Für andere Referenztypen als `string` gibt `!=` den Wert true zurück, wenn seine beiden Operanden auf verschiedene Objekte verweisen.  Für den `string`\-Typ vergleicht `!=` die Werte der Zeichenfolgen.  
  
 Benutzerdefinierte Werttypen können den Operator `!=` überladen \(siehe [Operator](../../../csharp/language-reference/keywords/operator.md)\).  Dies ist auch bei benutzerdefinierten Referenztypen möglich, obwohl sich `!=` standardmäßig sowohl für vordefinierte als auch für benutzerdefinierte Referenztypen wie oben beschrieben verhält.  Wenn `!=` überladen wird, muss auch [\=\=](../../../csharp/language-reference/operators/equality-comparison-operator.md) überladen werden.  Operationen mit Ganzzahltypen sind bei der Enumeration grundsätzlich zulässig.  
  
## Beispiel  
 [!CODE [csRefOperators#33](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#33)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)