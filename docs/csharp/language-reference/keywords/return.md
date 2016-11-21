---
title: "return (C#-Referenz) | Microsoft Docs"
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
  - "return_CSharpKeyword"
  - "return"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "return-Schlüsselwort [C#]"
  - "return-Anweisung [C#]"
ms.assetid: 6da6e152-5b58-4448-8f3f-470dd0617ecd
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# return (C#-Referenz)
Mit der `return`\-Anweisung wird die Ausführung der Methode, in der sie auftritt, beendet. Die Steuerung wird an die aufrufende Methode zurückgegeben.  Sie kann auch einen optionalen Wert zurückgeben.  Wenn die Methode ein `void`\-Typ ist, kann auf die `return`\-Anweisung verzichtet werden.  
  
 Wenn sich die return\-Anweisung innerhalb eines `try`\-Blocks befindet, wird der `finally`\-Block, falls vorhanden, ausgeführt, bevor das Steuerelement zur aufrufenden Methode zurückkehrt.  
  
## Beispiel  
 Im folgenden Beispiel gibt die `A()`\-Methode die `Area`\-Variable als [double](../../../csharp/language-reference/keywords/double.md)\-Wert zurück.  
  
 [!CODE [csrefKeywordsJump#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#6)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [return\-Anweisung](/visual-cpp/cpp/return-statement-cpp)   
 [Sprunganweisungen](../../../csharp/language-reference/keywords/jump-statements.md)