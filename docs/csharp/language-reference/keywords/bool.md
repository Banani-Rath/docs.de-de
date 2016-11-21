---
title: "bool (C#-Referenz) | Microsoft Docs"
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
  - "bool_CSharpKeyword"
  - "bool"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "bool-Schlüsselwort [C#]"
ms.assetid: 551cfe35-2632-4343-af49-33ad12da08e2
caps.latest.revision: 30
caps.handback.revision: 30
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# bool (C#-Referenz)
Das `bool`\-Schlüsselwort ist ein Alias von <xref:System.Boolean?displayProperty=fullName>.  Es wird verwendet, um Variablen zur Speicherung der booleschen Werte [true](../../../csharp/language-reference/keywords/true.md) und [false](../../../csharp/language-reference/keywords/false.md) zu deklarieren.  
  
> [!NOTE]
>  Wenn Sie eine boolesche Variable benötigen, die auch den Wert `null` annehmen kann, verwenden Sie `bool?`.  Weitere Informationen finden Sie unter [Typen, die NULL\-Werte zulassen](../../../csharp/programming-guide/nullable-types/index.md).  
  
## Literale  
 Sie können einer `bool`\-Variablen einen booleschen Wert zuweisen.  Sie können auch einen Ausdruck zuweisen, durch den eine `bool`\-Variable als `bool` ausgewertet wird.  
  
 [!CODE [csrefKeywordsTypes#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#1)]  
  
 Der Standardwert einer `bool`\-Variablen ist `false`.  Der Standardwert einer `bool?`\-Variablen ist `null`.  
  
## Konvertierungen  
 In C\+\+ kann ein Wert vom Typ `bool` in einen Wert vom Typ `int` konvertiert werden. Mit anderen Worten: `false` entspricht 0, und `true` entspricht Werten ungleich 0.  In C\# findet keine Konvertierung zwischen dem `bool`\-Typ und anderen Datentypen statt.  Zum Beispiel ist die folgende `if`\-Anweisung in C\# ungültig:  
  
 [!CODE [csrefKeywordsTypes#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#2)]  
  
 Um eine Variable vom Typ `int` zu testen, müssen Sie sie explizit mit einem Wert, beispielsweise 0 \(null\), vergleichen. Beispiel:  
  
 [!CODE [csrefKeywordsTypes#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#3)]  
  
## Beispiel  
 In diesem Beispiel geben Sie über die Tastatur ein Zeichen ein, woraufhin das Programm prüft, ob das eingegebene Zeichen ein Buchstabe ist.  Falls ja, wird überprüft, ob der Buchstabe in Groß\- oder Kleinschreibung eingegeben wurde.  Diese Überprüfungen werden mit <xref:System.Char.IsLetter%2A> und <xref:System.Char.IsLower%2A> ausgeführt, die beide den `bool`\-Typ zurückgeben:  
  
 [!CODE [csrefKeywordsTypes#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#4)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Tabelle ganzzahliger Typen](../../../csharp/language-reference/keywords/integral-types-table.md)   
 [Tabelle integrierter Typen](../../../csharp/language-reference/keywords/built-in-types-table.md)   
 [Tabelle für implizite numerische Konvertierungen](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)   
 [Tabelle für explizite numerische Konvertierungen](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)