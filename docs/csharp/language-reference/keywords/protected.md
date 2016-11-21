---
title: "protected (C#-Referenz) | Microsoft Docs"
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
  - "protected"
  - "protected_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "protected-Schlüsselwort [C#]"
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# protected (C#-Referenz)
Bei dem `protected`\-Schlüsselwort handelt es sich um einen Zugriffsmodifizierer für Member.  Ein geschützter Member ist innerhalb seiner Klasse und für abgeleitete Klasseninstanzen zugreifbar.  Einen Vergleich von `protected` mit den anderen Zugriffsmodifizierern finden Sie unter [Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md).  
  
## Beispiel  
 Auf einen geschützten Member einer Basisklasse kann nur dann in einer abgeleiteten Klasse zugegriffen werden, wenn der Zugriff über den abgeleiteten Klassentyp erfolgt.  Betrachten Sie z. B. das folgende Codesegment:  
  
 [!CODE [csrefKeywordsModifiers#11](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#11)]  
  
 Die Anweisung `a.x = 10` führt zu einem Fehler, da sie innerhalb der statischen Main\-Methode und nicht als Instanz der Klasse B erstellt wird.  
  
 Strukturmember können nicht geschützt werden, da die Struktur nicht vererbt werden kann.  
  
## Beispiel  
 In diesem Beispiel wird die `DerivedPoint`\-Klasse von `Point` abgeleitet.  Aus diesem Grund kann direkt von der abgeleiteten Klasse auf die geschützten Member der Basisklasse zugegriffen werden.  
  
 [!CODE [csrefKeywordsModifiers#12](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#12)]  
  
 Wenn Sie die Zugriffsebenen von `x` und `y` in [private](../../../csharp/language-reference/keywords/private.md) ändern, gibt der Compiler folgende Fehlermeldungen aus:  
  
 `'Point.y' is inaccessible due to its protection level.`  
  
 `'Point.x' is inaccessible due to its protection level.`  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Zugriffsmodifizierer](../../../csharp/language-reference/keywords/access-modifiers.md)   
 [Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md)   
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)   
 [public](../../../csharp/language-reference/keywords/public.md)   
 [Private](../../../csharp/language-reference/keywords/private.md)   
 [interne](../../../csharp/language-reference/keywords/internal.md)