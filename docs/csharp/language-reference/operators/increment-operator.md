---
title: "Operator&#160;++ (C#-Referenz) | Microsoft Docs"
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
  - "++_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "++ (Operator) [C#]"
  - "Inkrementoperator (++) [C#]"
ms.assetid: e9dec353-070b-44fb-98ed-eb8fdf753feb
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator&#160;++ (C#-Referenz)
Der Inkrementoperator \(`++`\) erhöht seinen Operanden um 1. Der Inkrementoperator kann vor oder hinter seinem Operanden angezeigt werden: `++variable` und `variable++`.  
  
## Hinweise  
 Die erste Form stellt eine Präfixinkrementoperation dar. Das Ergebnis der Operation ist der Wert des Operanden, nachdem er erhöht worden ist.  
  
 Die zweite Form stellt eine Postfixinkrementoperation dar. Das Ergebnis der Operation ist der Wert des Operanden, bevor er erhöht wird.  
  
 Für alle numerischen Typen und Enumerationstypen sind Inkrementoperatoren vordefiniert. Benutzerdefinierte Typen können den Operator `++` überladen. Operationen mit Ganzzahltypen sind grundsätzlich auch für Aufzählungen \(enum\) zulässig.  
  
## Beispiel  
 [!CODE [csRefOperators#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#3)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)