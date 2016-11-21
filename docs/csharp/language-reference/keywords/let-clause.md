---
title: "let-Klausel (C#-Referenz) | Microsoft Docs"
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
  - "let_CSharpKeyword"
  - "let"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Let-Klausel [C#]"
  - "let-Schlüsselwort [C#]"
ms.assetid: 13c9c1a4-ce57-48ef-8e1b-4c2a59b99fb4
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# let-Klausel (C#-Referenz)
Bei Abfrageausdrücken ist es gelegentlich nützlich, das Ergebnis eines Unterausdrucks zu speichern, um es in nachfolgenden Klauseln zu verwenden.  Verwenden Sie dazu das `let`\-Schlüsselwort, das eine neue Bereichsvariable erstellt und sie mit dem von Ihnen bereitgestellten Ergebnis des Ausdrucks initialisiert.  Nachdem die Bereichsvariable mit einem Wert initialisiert wurde, kann sie nicht mehr zum Speichern eines anderen Werts verwendet werden.  Wenn die Bereichsvariable jedoch einen abfragbaren Typ enthält, kann sie abgefragt werden.  
  
## Beispiel  
 Im folgenden Beispiel wird `let` auf zwei Weisen verwendet:  
  
1.  Um einen Enumerable\-Typ zu erstellen, der selbst abgefragt werden kann.  
  
2.  Um es der Abfrage zu ermöglichen, `ToLower` nur ein Mal für die Bereichsvariable `word` aufzurufen.  Wenn Sie `let` nicht verwenden würden, müssten Sie `ToLower` in jedem Prädikat in der `where`\-Klausel aufrufen.  
  
 [!CODE [cscsrefQueryKeywords#28](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#28)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [Abfrageschlüsselwörter \(LINQ\)](../../../csharp/language-reference/keywords/query-keywords.md)   
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [Getting Started with LINQ in C\#](../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md)   
 [Gewusst wie: Behandeln von Ausnahmen in Abfrageausdrücken](../../../csharp/programming-guide/linq-query-expressions/how-to-handle-exceptions-in-query-expressions.md)