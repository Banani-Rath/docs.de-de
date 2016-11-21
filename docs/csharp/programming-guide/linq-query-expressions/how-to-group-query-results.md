---
title: "Gewusst wie: Gruppieren von Abfrageergebnissen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "group-Klausel (Beispiele) [LINQ in C#]"
  - "Gruppen [LINQ in C#]"
  - "Abfragen [LINQ in C#], Gruppieren"
  - "Abfrageausdrücke [LINQ in C#], Gruppieren"
ms.assetid: ee981053-3392-4245-a8c2-b3730211da0d
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Gruppieren von Abfrageergebnissen (C#-Programmierhandbuch)
Das Gruppieren ist eine der leistungsstärksten Funktionen von [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)].  In den folgenden Beispielen wird gezeigt, wie Daten auf verschiedene Weisen gruppiert werden:  
  
-   Anhand einer einzelnen Eigenschaft.  
  
-   Anhand des ersten Buchstabens einer Zeichenfolgeneigenschaft.  
  
-   Anhand eines berechneten numerischen Bereichs.  
  
-   Anhand eines booleschen Prädikats oder anderen Ausdrucks.  
  
-   Anhand eines zusammengesetzten Schlüssels.  
  
 Darüber hinaus projizieren die letzten beiden Abfragen die Ergebnisse in einen neuen anonymen Typ, der nur den Vor\- und Nachnamen des Studenten enthält.  Weitere Informationen finden Sie unter [group\-Klausel](../../../csharp/language-reference/keywords/group-clause.md).  
  
## Beispiel  
 Alle Beispiele in diesem Thema nutzen die folgenden Hilfsklassen und Datenquellen.  
  
 [!CODE [csProgGuideLINQ#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#15)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Sie Quellelemente gruppieren können, indem Sie eine einzelne Eigenschaft des Elements als Gruppenschlüssel verwenden.  In diesem Fall ist der Schlüssel ein `string`, der Nachname des Studenten.  Es ist auch möglich, eine Teilzeichenfolge für den Schlüssel zu verwenden.  Der Gruppierungsvorgang verwendet den Standardgleichheitsvergleich für den Typ.  
  
 Fügen Sie die folgende Methode in die `StudentClass`\-Klasse ein.  Ändern Sie die Aufrufanweisung in der `Main`\-Methode in `sc.GroupBySingleProperty()`.  
  
 [!CODE [csProgGuideLINQ#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#17)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Sie Quellelemente gruppieren können, indem Sie einen anderen Gruppenschlüssel als die Objekteigenschaft verwenden.  In diesem Beispiel ist der Schlüssel der erste Buchstabe des Nachnamens des Studenten.  
  
 Fügen Sie die folgende Methode in die `StudentClass`\-Klasse ein.  Ändern Sie die Aufrufanweisung in der `Main`\-Methode in `sc.GroupBySubstring()`.  
  
 [!CODE [csProgGuideLINQ#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#18)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Sie Quellelemente gruppieren können, indem Sie einen numerischen Bereich als Gruppenschlüssel verwenden.  Die Abfrage projiziert dann die Ergebnisse in einen anonymen Typ, der nur den Vor\- und Nachnamen sowie den prozentualen Bereich des Studenten enthält.  Der anonyme Typ wird verwendet, da nicht das gesamte `Student`\-Objekt zur Anzeige der Ergebnisse verwendet werden muss.  `GetPercentile` ist eine Hilfsfunktion, mit der ein prozentualer Bereich anhand der Durchschnittsbewertung des Studenten berechnet wird.  Die Methode gibt einen ganzzahligen Wert zwischen 0 und 10 zurück.  
  
 [!CODE [csProgGuideLINQ#50](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#50)]  
  
 Fügen Sie die folgende Methode in die `StudentClass`\-Klasse ein.  Ändern Sie die Aufrufanweisung in der `Main`\-Methode in `sc.GroupByRange()`.  
  
 [!CODE [csProgGuideLINQ#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#19)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Sie Quellelemente gruppieren können, indem Sie einen booleschen Vergleichsausdruck verwenden.  In diesem Beispiel überprüft der boolesche Ausdruck, ob die Prüfungsdurchschnittsbewertung eines Studenten größer als 75 ist.  Wie in vorherigen Beispielen werden die Ergebnisse in einen anonymen Typ projiziert, da nicht das gesamte Quellelement benötigt wird.  Beachten Sie, dass die Eigenschaften im anonymen Typ zu Eigenschaften auf dem `Key`\-Member werden und beim Ausführen der Abfrage der Zugriff auf sie anhand des Namens möglich ist.  
  
 Fügen Sie die folgende Methode in die `StudentClass`\-Klasse ein.  Ändern Sie die Aufrufanweisung in der `Main`\-Methode in `sc.GroupByBoolean()`.  
  
 [!CODE [csProgGuideLINQ#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#20)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie Sie einen anonymen Typ zum Kapseln eines Schlüssels mit mehreren Werten verwenden können.  In diesem Beispiel ist der erste Schlüsselwert der erste Buchstabe des Nachnamens des Studenten.  Der zweite Schlüsselwert ist ein boolescher Wert, der angibt, ob der Student in der ersten Prüfung einen Wert über 85 erzielt hat.  Sie können die Gruppen anhand jeder Eigenschaft im Schlüssel sortieren.  
  
 Fügen Sie die folgende Methode in die `StudentClass`\-Klasse ein.  Ändern Sie die Aufrufanweisung in der `Main`\-Methode in `sc.GroupByCompositeKey()`.  
  
 [!CODE [csProgGuideLINQ#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#21)]  
  
## Kompilieren des Codes  
 Kopieren Sie jede Methode, die Sie testen möchten, in die `StudentClass`\-Klasse.  Fügen Sie der `Main`\-Methode eine Aufrufanweisung für die Methode hinzu, und drücken Sie F5.  
  
 Wenn Sie diese Methoden an die eigene Anwendung anpassen, beachten Sie, dass LINQ [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] Version 3.5 oder 4 erfordert und dass das Projekt einen Verweis auf System.Core.dll enthalten und eine Direktive für System.Linq verwenden muss.  LINQ to SQL\-, LINQ to XML\- und LINQ to DataSet\-Typen erfordern zusätzliche using\-Direktiven und \-Verweise.  Weitere Informationen hierzu finden Sie unter [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md).  
  
## Siehe auch  
 <xref:System.Linq.Enumerable.GroupBy%2A>   
 <xref:System.Linq.IGrouping%602>   
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [group\-Klausel](../../../csharp/language-reference/keywords/group-clause.md)   
 [Anonyme Typen](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)   
 [Gewusst wie: Ausführen einer Unterabfrage für eine Gruppierungsoperation](../../../csharp/programming-guide/linq-query-expressions/how-to-perform-a-subquery-on-a-grouping-operation.md)   
 [Gewusst wie: Erstellen einer geschachtelten Gruppe](../../../csharp/programming-guide/linq-query-expressions/how-to-create-a-nested-group.md)   
 [Grouping Data](../../../visual-basic/programming-guide/concepts/linq/grouping-data.md)