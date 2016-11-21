---
title: "public (C#-Referenz) | Microsoft Docs"
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
  - "public"
  - "public_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "public-Schlüsselwort [C#]"
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# public (C#-Referenz)
Bei dem `public`\-Schlüsselwort handelt es sich um einen Zugriffsmodifizierer für Typen und Typmember.  Öffentlicher Zugriff stellt die am wenigsten eingeschränkte Zugriffsebene dar.  Es gibt keine Beschränkungen auf zugreifende öffentliche Member, wie in diesem Beispiel gezeigt wird:  
  
```  
class SampleClass  
{  
    public int x; // No access restrictions.  
}  
```  
  
 Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md) und [Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md).  
  
## Beispiel  
 Im folgenden Beispiel werden die beiden Klassen `PointTest` und `MainClass` deklariert.  Auf die öffentlichen Member `x` und `y` von `PointTest` wird direkt von `MainClass` aus zugegriffen.  
  
 [!CODE [csrefKeywordsModifiers#13](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#13)]  
  
 Wenn Sie die Zugriffsebene von `public` in [private](../../../csharp/language-reference/keywords/private.md) oder [protected](../../../csharp/language-reference/keywords/protected.md) ändern, wird die folgende Fehlermeldung angezeigt:  
  
 Der Zugriff auf "PointTest.y" ist aufgrund der Sicherheitsebene nicht möglich.  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Zugriffsmodifizierer](../../../csharp/language-reference/keywords/access-modifiers.md)   
 [Zugriffsebenen](../../../csharp/language-reference/keywords/accessibility-levels.md)   
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)   
 [Private](../../../csharp/language-reference/keywords/private.md)   
 [protected](../../../csharp/language-reference/keywords/protected.md)   
 [interne](../../../csharp/language-reference/keywords/internal.md)