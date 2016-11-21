---
title: ". Operator (C#-Referenz) | Microsoft Docs"
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
  - "._CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - ". Operator [C#]"
  - "Punktoperator (.) [C#]"
  - "Memberzugriffsoperator (.) [C#]"
ms.assetid: a1f54b52-b686-4ae5-a48e-a2a9ebd0eb7b
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# . Operator (C#-Referenz)
Der Punktoperator \(`.`\) wird für Memberzugriff verwendet.  Der Punktoperator gibt einen Member von einem Typ oder einem Namespace an.  Der Punktoperator wird beispielsweise verwendet, um auf bestimmte Methoden in .NET Framework\-Klassenbibliotheken zuzugreifen:  
  
 [!CODE [csRefOperators#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#16)]  
  
 Betrachten Sie z. B. die folgende Klasse:  
  
 [!CODE [csRefOperators#17](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#17)]  
  
 [!CODE [csRefOperators#18](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#18)]  
  
 Die `s`\-Variable weist die beiden Member `a` und `b` auf. Um auf sie zuzugreifen, wird der Punktoperator verwendet:  
  
 [!CODE [csRefOperators#19](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#19)]  
  
 Der Punkt wird auch dazu verwendet, gekennzeichnete Namen zu verwenden, also Namen, die z. B. den Namespace oder die Schnittstelle angeben, wozu sie gehören.  
  
 [!CODE [csRefOperators#20](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#20)]  
  
 Durch die using\-Direktive wird ein Teil der Namenskennzeichnung optional:  
  
 [!CODE [csRefOperators#21](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#21)]  
  
 Ist aber ein Bezeichner mehrdeutig, muss er gekennzeichnet werden:  
  
 [!CODE [csRefOperators#22](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#22)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)