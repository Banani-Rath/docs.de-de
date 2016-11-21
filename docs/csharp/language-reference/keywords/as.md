---
title: "as (C#-Referenz) | Microsoft Docs"
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
  - "as_CSharpKeyword"
  - "as"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "as-Schlüsselwort [C#]"
  - "Typkonvertierung [C#], as-Schlüsselwort"
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# as (C#-Referenz)
Sie können den `as`\-Operator verwenden, um bestimmte Typen von Konvertierungen zwischen kompatiblen Referenztypen oder [Typ, der NULL\-Werte zulässt,](../../../csharp/programming-guide/nullable-types/index.md) auszuführen.  Im Folgenden ein Codebeispiel.  
  
 [!CODE [csrefKeywordsOperator#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#1)]  
  
## Hinweise  
 Der Operator `as` kann mit einem Umwandlungsvorgang verglichen werden.  Wenn die Konvertierung nicht möglich ist, gibt `as``null` zurück, anstatt eine Ausnahme auszulösen.  Betrachten Sie das folgende Beispiel:  
  
```  
expression as type  
```  
  
 Der Code entspricht dem folgenden Ausdruck äquivalent, außer dass die `expression`\-Variable wird nur einmal ausgewertet.  
  
```  
expression is type ? (type)expression : (type)null  
```  
  
 Beachten Sie, dass der `as`\-Operator nur Verweiskonvertierungen, auf NULL festlegbare Konvertierungen und Boxingkonvertierungen ausführt.  Der `as`\-Operator kann andere Konvertierungen, wie benutzerdefinierte Konvertierungen nicht ausführen, die stattdessen ausgeführt werden sollen, indem Umwandlungsausdrücke verwendet.  
  
## Beispiel  
 [!CODE [csrefKeywordsOperator#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#2)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [is](../../../csharp/language-reference/keywords/is.md)   
 [Operator ?:](../../../csharp/language-reference/operators/conditional-operator.md)   
 [Operatorschlüsselwörter](../../../csharp/language-reference/keywords/operator-keywords.md)