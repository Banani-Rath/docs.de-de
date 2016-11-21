---
title: "Gewusst wie: Schreiben von LINQ-Abfragen in C# | Microsoft Docs"
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
  - "Abfragen [LINQ in C#], Schreiben"
  - "Abfrageausdrücke [LINQ in C#], Schreiben von Abfragen"
  - "Schreiben von LINQ-Abfragen"
ms.assetid: 45e47fcc-cfa1-4b72-b161-d038ae87bd23
caps.latest.revision: 25
caps.handback.revision: 25
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Schreiben von LINQ-Abfragen in C#
Dieses Thema zeigt die drei Methoden, mit denen Sie eine [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)]\-Abfrage in C\# schreiben können:  
  
1.  Verwenden Sie die Abfragesyntax.  
  
2.  Verwenden Sie die Methodensyntax.  
  
3.  Verwenden Sie eine Kombination aus Abfragesyntax und Methodensyntax.  
  
 In den folgenden Beispielen werden einige einfache [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)]\-Abfragen veranschaulicht, indem sie jeden zuvor aufgelisteten Ansatz verwenden.  Im Allgemeinen muss die Regel wann immer möglich \(1\) verwenden und wann immer notwendig \(2\) und \(3\) verwenden.  
  
> [!NOTE]
>  Diese Abfragen basieren auf einfachen speicherinternen Auflistungen; die grundlegende Syntax ist jedoch mit der in [!INCLUDE[vbtecdlinq](../../../csharp/includes/vbtecdlinq_md.md)] und [!INCLUDE[sqltecxlinq](../../../csharp/programming-guide/concepts/linq/includes/sqltecxlinq_md.md)] verwendeten identisch.  
  
## Beispiel  
  
## Abfragesyntax  
 Es wird empfohlen, die meisten Abfragen mit *Abfragesyntax* zu schreiben, um *Abfrageausdrücke* zu erstellen.  Im folgenden Beispiel werden drei Abfrageausdrücke veranschaulicht.  Der erste Abfrageausdruck zeigt, wie Ergebnisse gefiltert oder eingeschränkt werden, indem Sie Bedingungen mit einer `where`\-Klausel anwenden.  Er gibt alle Elemente in der Quellsequenz zurück, deren Werte größer als 7 oder kleiner als 3 sind.  Der zweite Ausdruck zeigt, wie die zurückgegebenen Ergebnisse sortiert werden.  Der dritte Ausdruck veranschaulicht, wie Ergebnisse anhand eines Schlüssels gruppiert werden.  Diese Abfrage gibt zwei Gruppen basierend auf dem Buchstaben des Worts zurück.  
  
 [!CODE [csProgGuideLINQ#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#5)]  
  
 Beachten Sie, dass die Abfragen vom Typ <xref:System.Collections.Generic.IEnumerable%601> sind.  Alle diese Abfragen konnten mit `var` geschrieben werden, wie im folgenden Beispiel gezeigt:  
  
 `var query = from num in numbers...`  
  
 In jedem vorherigen Beispiel werden die Abfragen erst dann ausgeführt, wenn Sie die Abfragevariable in einer `foreach`\-Anweisung durchlaufen.  Weitere Informationen hierzu finden Sie unter [Introduction to LINQ Queries \(C\#\)](../../../csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).  
  
## Beispiel  
  
## Methodensyntax  
 Einige Abfrageoperationen müssen als Methodenaufruf ausgedrückt werden.  Die am häufigsten verwendeten Methoden sind jene, die einzelne numerische Werte zurückgeben, z. B. <xref:System.Linq.Enumerable.Sum%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A>, <xref:System.Linq.Enumerable.Average%2A>.  Diese Methoden müssen immer zuletzt in einer Abfrage aufgerufen werden, da sie nur einen einzelnen Wert darstellen und nicht als Quelle für eine zusätzliche Abfrageoperation dienen.  Das folgende Beispiel zeigt einen Methodenaufruf in einem Abfrageausdruck:  
  
 [!CODE [csProgGuideLINQ#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#6)]  
  
## Beispiel  
 Wenn die Methode über Parameter verfügt, werden diese in Form eines [Lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)\-Ausdrucks bereitgestellt, wie im folgenden Beispiel gezeigt:  
  
 [!CODE [csProgGuideLINQ#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#7)]  
  
 In den vorherigen Abfragen wird nur Abfrage 4 sofort ausgeführt.  Das liegt daran, dass sie einen einzelnen Wert und nicht eine generische <xref:System.Collections.Generic.IEnumerable%601>\-Auflistung zurückgibt.  Die Methode selbst muss `foreach` verwenden, um den Wert zu berechnen.  
  
 Alle diese vorherigen Abfragen können mithilfe der impliziten Typisierung mit [var](../../../csharp/language-reference/keywords/var.md) geschrieben werden, wie im folgenden Beispiel gezeigt wird:  
  
 [!CODE [csProgGuideLINQ#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#8)]  
  
## Beispiel  
  
## Gemischte Abfrage und Methodensyntax  
 Dieses Beispiel zeigt, wie die Methodensyntax für Ergebnisse einer Abfrageklausel verwendet wird.  Schließen Sie den Abfrageausdruck in Klammern ein, wenden Sie dann den Punktoperator an, und rufen Sie die Methode auf.  Im folgenden Beispiel gibt Abfrage 7 eine Anzahl der Zahlen zurück, deren Wert zwischen 3 und 7 liegt.  Im Allgemeinen ist es jedoch besser, eine zweite Variable zum Speichern der Ergebnisse des Methodenaufrufs zu verwenden.  Auf diese Weise kann die Abfrage nicht so leicht mit den Ergebnissen der Abfrage verwechselt werden.  
  
 [!CODE [csProgGuideLINQ#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#9)]  
  
 Da Abfrage 7 einen einzelnen Wert und keine Auflistung zurückgibt, wird die Abfrage sofort ausgeführt.  
  
 Die vorherige Abfrage kann mithilfe der impliziten Typisierung mit `var` folgendermaßen geschrieben werden:  
  
```  
var numCount = (from num in numbers...  
```  
  
 Sie kann folgendermaßen in Methodensyntax geschrieben werden:  
  
```  
var numCount = numbers.Where(n => n < 3 || n > 7).Count();  
```  
  
 Sie kann folgendermaßen mit expliziter Typisierung geschrieben werden:  
  
```  
int numCount = numbers.Where(n => n < 3 || n > 7).Count();  
```  
  
## Siehe auch  
 [LINQ \(Language\-Integrated Query\)](../Topic/LINQ%20\(Language-Integrated%20Query\).md)   
 [Walkthrough: Writing Queries in C\#](../../../csharp/programming-guide/concepts/linq/walkthrough-writing-queries-linq.md)   
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [where\-Klausel](../../../csharp/language-reference/keywords/where-clause.md)