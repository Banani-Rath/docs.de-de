---
title: "out (C#-Referenz) | Microsoft Docs"
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
  - "out_CSharpKeyword"
  - "out"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "out [C#]"
  - "out-Schlüsselwort [C#]"
ms.assetid: 7e911a0c-3f98-4536-87be-d539b7536ca8
caps.latest.revision: 30
caps.handback.revision: 30
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# out (C#-Referenz)
Sie können das kontextbezogene Schlüsselwort `out` in zwei Kontexten \(jeder ist ein Link zu detaillierten Informationen\) als einen [Parametermodifizierer](../../../csharp/language-reference/keywords/out-parameter-modifier.md) oder in [Parameterdeklarationen vom Typ "generisch"](../../../csharp/language-reference/keywords/out-generic-modifier.md) in Schnittstellen und Delegaten verwenden.  Dieses Thema behandelt die Parametermodifizierer; in diesem [anderen Thema](../../../csharp/language-reference/keywords/out-generic-modifier.md) finden Sie Informationen über die Parameterdeklarationen vom Typ "generisch".  
  
 Das Schlüsselwort `out` bewirkt, dass Argumente per Verweis übergeben werden.  Dies entspricht dem Schlüsselwort [ref](../../../csharp/language-reference/keywords/ref.md), mit Ausnahme davon, dass bei`ref` die Variable initialisiert sein muss, bevor sie übergeben wird.  Um einen Parameter `out` zu verwenden, müssen sowohl die Methodendefinition als auch die aufrufende Methode das Schlüsselwort `out` explizit verwenden.  Beispiel:  
  
 [!CODE [csrefKeywordsMethodParams#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#1)]  
  
 Auch wenn Variablen, die als `out`\-Argumente übergeben werden, nicht initialisiert sein müssen, bevor Sie übergeben werden, muss die aufgerufene Methode einen Wert zuweisen, bevor die Methode zurückgegeben wird.  
  
 Obwohl die Schlüsselwörter `ref` und `out` unterschiedliche Laufzeitverhalten hervorrufen, gelten sie zum Zeitpunkt der Kompilierung nicht als Teil der Methodensignatur.  Aus diesem Grund können die Methoden nicht überladen werden, wenn der einzige Unterschied darin besteht, dass eine Methode ein `ref`\-Argument übernimmt und die andere ein `out`\-Argument.  Der folgende Code wird z. B. nicht kompiliert:  
  
 [!CODE [csrefKeywordsMethodParams#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#2)]  
  
 Überladen ist möglich; wenn jedoch eine Methode ein `ref`\- oder `out`\-Argument übernimmt und die andere keines der beiden, gilt Folgendes:  
  
 [!CODE [csrefKeywordsMethodParams#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#3)]  
  
 Eigenschaften sind keine Variablen und können daher nicht als `out`\-Parameter übergeben werden.  
  
 Weitere Informationen zum Übergeben von Arrays finden Sie unter [Übergeben von Arrays mithilfe von "ref" und "out"](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).  
  
 Sie können keines der beiden Schlüsselwörter `ref` und `out` für die folgenden Methodentypen verwenden:  
  
-   Async\-Methoden, die Sie mit dem [async](../../../csharp/language-reference/keywords/async.md)\-Modifizierer definieren.  
  
-   Iterator\-Methoden, die eine [yield return](../../../csharp/language-reference/keywords/yield.md)\- oder `yield break`\-Anweisung enthalten.  
  
## Beispiel  
 Das Deklarieren einer `out`\-Methode ist nützlich, wenn eine Methode mehrere Werte zurückgeben soll.  Im folgenden Beispiel wird `out` verwendet, um mit einem Methodenaufruf drei Variablen zurückzugeben.  Beachten Sie, dass das dritte Argument Null zugewiesen ist.  Dadurch können Methoden Werte optional zurückgeben.  
  
 [!CODE [csrefKeywordsMethodParams#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#4)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)