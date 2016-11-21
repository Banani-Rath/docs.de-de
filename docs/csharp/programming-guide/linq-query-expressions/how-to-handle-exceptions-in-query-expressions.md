---
title: "Gewusst wie: Behandeln von Ausnahmen in Abfrageausdr&#252;cken (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Ausnahmen [C#], LINQ-Abfragen"
  - "Abfragen [LINQ in C#], Ausnahmen"
  - "Abfrageausdrücke [LINQ in C#], Ausnahmen"
ms.assetid: 4ce6c081-7731-4b8f-b4fa-d947f165a18a
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Behandeln von Ausnahmen in Abfrageausdr&#252;cken (C#-Programmierhandbuch)
Es ist möglich, eine Methode im Kontext eines Abfrageausdrucks aufzurufen.  Sie sollten es jedoch vermeiden, eine Methode in einem Abfrageausdruck aufzurufen, wenn dies zu unerwünschten Nebeneffekten führt, z. B. zum Ändern des Inhalts der Datenquelle oder zum Auslösen einer Ausnahme.  Dieses Beispiel zeigt, wie Sie verhindern können, dass Ausnahmen ausgelöst werden, wenn Sie Methoden in einem Abfrageausdruck aufrufen, ohne gegen die allgemeinen [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)]\-Richtlinien zur Ausnahmebehandlung zu verstoßen.  Diese Richtlinien besagen, dass spezielle Ausnahmen abgefangen werden können, wenn Sie wissen, warum sie in einem bestimmten Kontext ausgelöst werden.  Weitere Informationen finden Sie unter [Best Practices für Ausnahmen](../Topic/Best%20Practices%20for%20Exceptions.md).  
  
 Im letzten Beispiel wird gezeigt, wie Sie Fälle, in denen die Ausgabe einer Ausnahme während der Ausführung einer Abfrage erforderlich ist, behandeln können.  
  
## Beispiel  
 Im folgenden Beispiel wird gezeigt, wie Ausnahmebehandlungscode außerhalb eines Abfrageausdrucks verschoben wird.  Dies ist nur möglich, wenn die Methode von keiner für die Abfrage lokalen Variablen abhängig ist.  
  
 [!CODE [csProgGuideLINQ#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#10)]  
  
## Beispiel  
 In einigen Fällen ist die beste Antwort auf eine Ausnahme, die in einer Abfrage ausgelöst wird, das unmittelbare Anhalten des Abfragevorgangs.  Im folgenden Beispiel wird gezeigt, wie Ausnahmen, die in einem Abfragetext ausgelöst werden könnten, behandelt werden.  Annahme: `SomeMethodThatMightThrow` kann potenziell eine Ausnahme auslösen, woraufhin die Ausführung der Abfrage beendet werden muss.  
  
 Beachten Sie, dass der `try`\-Block die `foreach`\-Schleife einschließt, und nicht die Abfrage selbst.  Das liegt daran, dass die `foreach`\-Schleife der Punkt ist, an dem die Abfrage eigentlich ausgeführt wird.  Weitere Informationen hierzu finden Sie unter [Introduction to LINQ Queries \(C\#\)](../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).  
  
 [!CODE [csProgGuideLINQ#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#12)]  
  
## Kompilieren des Codes  
  
-   Erstellen Sie ein [!INCLUDE[vs_current_short](../../../csharp/programming-guide/classes-and-structs/includes/vs_current_short_md.md)]\-Projekt für .NET Framework, Version 3.5.  Standardmäßig weist das Projekt einen Verweis auf System.Core.dll und eine `using`\-Direktive für den System.Linq\-Namespace auf.  
  
-   Kopieren Sie den Code in Ihr Projekt.  
  
-   Drücken Sie F5, um das Programm zu kompilieren und auszuführen.  
  
 Drücken Sie eine beliebige Taste, um das Konsolenfenster zu schließen.  
  
## Siehe auch  
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)