---
title: "#else (C#-Referenz) | Microsoft Docs"
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
  - "#else"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "#else-Direktive [C#]"
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# #else (C#-Referenz)
Mit `#else` kann eine zusammengesetzte bedingte Direktive erstellt werden, sodass der gesamte Code zwischen `#else` und dem nachfolgenden `#endif` vom Compiler ausgewertet wird, wenn keiner der Ausdrücke in den voranstehenden [\#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md)\-Direktiven oder \(optionalen\) [\#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md)\-Direktiven mit `true` ausgewertet wurde.  
  
## Hinweise  
 [\#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) muss als nächste Präprozessordirektive nach `#else` folgen.  Ein Beispiel zur Verwendung von `#else` finden Sie unter [\#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md).  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Präprozessordirektiven](../../../csharp/language-reference/preprocessor-directives/index.md)