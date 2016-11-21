---
title: "group-Klausel (C#-Referenz) | Microsoft Docs"
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
  - "group"
  - "group_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "group-Klausel [C#]"
  - "group-Schlüsselwort [C#]"
ms.assetid: c817242e-b12c-4baa-a57e-73ee138f34d1
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# group-Klausel (C#-Referenz)
Die `group`\-Klausel gibt eine Sequenz von <xref:System.Linq.IGrouping%602>\-Objekten zurück, die Null oder mehr Elemente enthält, die dem Schlüsselwert für die Gruppe entsprechen.  Zum Beispiel können Sie eine Sequenz von Zeichenfolgen nach dem ersten Buchstaben in jeder Zeichenfolge gruppieren.  In diesem Fall ist der erste Buchstabe der Schlüssel und weist den Typ [char](../../../csharp/language-reference/keywords/char.md) auf. Er wird in der `Key`\-Eigenschaft jedes <xref:System.Linq.IGrouping%602>\-Objekts gespeichert.  Der Compiler leitet den Typ des Schlüssels ab.  
  
 Sie können einen Abfrageausdruck mit einer `group`\-Klausel beenden, wie im folgenden Beispiel gezeigt:  
  
 [!CODE [cscsrefQueryKeywords#10](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#10)]  
  
 Wenn Sie zusätzliche Abfrageoperationen für jede Gruppe durchführen möchten, können Sie einen temporären Bezeichner festlegen, indem Sie das [into](../../../csharp/language-reference/keywords/into.md)\-Kontextschlüsselwort verwenden.  Wenn Sie `into` verwenden, müssen Sie mit der Abfrage fortfahren und sie letztendlich entweder mit einer `select`\-Anweisung oder einer anderen `group`\-Klausel wie im folgenden Auszug gezeigt beenden:  
  
 [!CODE [cscsrefQueryKeywords#11](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#11)]  
  
 Ausführlichere Beispiele zur Verwendung von `group` mit und ohne `into` finden Sie im Beispielabschnitt in diesem Thema.  
  
## Auflisten der Ergebnisse einer Gruppenabfrage  
 Da die <xref:System.Linq.IGrouping%602>\-Objekte, die durch eine `group`\-Abfrage erzeugt wurden, im Grunde eine Liste mit Listen sind, müssen Sie eine geschachtelte [foreach](../../../csharp/language-reference/keywords/foreach-in.md)\-Schleife verwenden, um auf die Elemente in jeder Gruppe zuzugreifen.  Die äußere Schleife durchläuft die Gruppenschlüssel, und die innere Schleife durchläuft die Elemente in der Gruppe.  Eine Gruppe verfügt möglicherweise über einen Schlüssel, jedoch nicht über Elemente.  Die `foreach`\-Schleife, die die Abfrage in den vorherigen Codebeispielen ausführt, sieht folgendermaßen aus:  
  
 [!CODE [cscsrefQueryKeywords#12](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#12)]  
  
## Schlüsseltypen  
 Gruppenschlüssel können ein beliebiger Typ sein, z. B. eine Zeichenfolge, ein integrierter numerischer Typ oder ein benutzerdefinierter benannter Typ bzw. anonymer Typ.  
  
### Gruppieren nach Zeichenfolge  
 In den vorherigen Codebeispielen wurde ein `char` verwendet.  Ein Zeichenfolgenschlüssel hätte mühelos stattdessen festgelegt werden können, z. B. der vollständige Nachname:  
  
 [!CODE [cscsrefQueryKeywords#13](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#13)]  
  
### Gruppieren nach bool  
 Im folgenden Beispiel wird die Verwendung eines booleschen Werts für einen Schlüssel gezeigt, um die Ergebnisse in zwei Gruppen zu teilen.  Beachten Sie, dass der Wert von einem Unterausdruck in der `group`\-Klausel erzeugt wird.  
  
 [!CODE [cscsrefQueryKeywords#14](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#14)]  
  
### Gruppieren nach numerischem Bereich  
 Im nächsten Beispiel wird ein Ausdruck verwendet, um numerische Gruppenschlüssel zu erstellen, die einen prozentualen Bereich darstellen.  Beachten Sie die Auswahl von [let](../../../csharp/language-reference/keywords/let-clause.md) als geeigneten Speicherort, um ein Ergebnis eines Methodenaufrufs zu speichern, sodass Sie die Methode nicht zweimal in der `group`\-Klausel aufrufen müssen.  Beachten Sie in der `group`\-Klausel auch, dass der Code überprüft, ob der Student keinen Durchschnitt von Null hat, um eine Nulldivisionsausnahme zu vermeiden.  Weitere Informationen zum sicheren Verwenden von Methoden in Abfrageausdrücken finden Sie unter [Gewusst wie: Behandeln von Ausnahmen in Abfrageausdrücken](../../../csharp/programming-guide/linq-query-expressions/how-to-handle-exceptions-in-query-expressions.md).  
  
 [!CODE [cscsrefQueryKeywords#15](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#15)]  
  
### Gruppieren nach zusammengesetzten Schlüsseln  
 Verwenden Sie einen zusammengesetzten Schlüssel, wenn Sie Elemente anhand mehr als einem Schlüssel gruppieren möchten.  Zusammengesetzte Schlüssel können Sie erstellen, indem Sie einen anonymen oder benannten Typ verwenden, der das Schlüsselelement enthalten soll.  Im folgenden Beispiel wird angenommen, dass eine Klasse `Person` mit Member mit den Namen `surname` und `city` deklariert wurde.  Die `group`\-Klausel bewirkt, dass eine separate Gruppe für jeden Satz an Personen mit dem gleichen Nachnamen und der gleichen Stadt erstellt werden kann.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 Verwenden Sie einen benannten Typ, wenn Sie die Abfragevariable an eine andere Methode übergeben müssen.  Erstellen Sie eine Sonderklasse mit automatisch implementierten Eigenschaften für die Schlüssel, und überschreiben Sie dann die <xref:System.Object.Equals%2A>\-Methode und die <xref:System.Object.GetHashCode%2A>\-Methode.  Sie können auch eine Struktur verwenden, sodass es nicht unbedingt erforderlich ist, diese Methoden zu überschreiben.  Weitere Informationen finden Sie unter [Gewusst wie: Implementieren einer einfachen Klasse mit automatisch implementierten Eigenschaften](../../../csharp/programming-guide/classes-and-structs/how-to-implement-a-lightweight-class-with-auto-implemented-properties.md) und [How to: Query for Duplicate Files in a Directory Tree \(LINQ\)](../Topic/How%20to:%20Query%20for%20Duplicate%20Files%20in%20a%20Directory%20Tree%20\(LINQ\).md).  Das zuletzt genannte Thema zeigt anhand eines Codebeispiels, wie ein zusammengesetzter Schlüssel mit einem benannten Typ verwendet wird.  
  
## Beispiel  
 Das folgende Beispiel zeigt das Standardmuster zum Sortieren von Quelldaten in Gruppen, wenn keine zusätzliche Abfragelogik auf die Gruppen angewendet wurde.  Dies wird als Gruppierung ohne Fortsetzung bezeichnet.  Die Elemente in einem Zeichenfolgenarray werden nach ihrem ersten Buchstaben gruppiert.  Das Ergebnis der Abfrage ist ein <xref:System.Linq.IGrouping%602>\-Typ, der eine öffentliche `Key`\-Eigenschaft vom Typ `char` und eine <xref:System.Collections.Generic.IEnumerable%601>\-Auflistung enthält, die wiederum jedes Element in der Gruppierung umfasst.  
  
 Das Ergebnis einer `group`\-Klausel ist eine Sequenz von Sequenzen.  Verwenden Sie daher zum Zugriff auf die einzelnen Elemente in jeder zurückgegebenen Gruppe eine geschachtelte `foreach`\-Schleife in der Schleife, die die Gruppenschlüssel wie im folgenden Beispiel gezeigt durchläuft.  
  
 [!CODE [cscsrefQueryKeywords#16](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#16)]  
  
## Beispiel  
 Dieses Beispiel zeigt, wie Sie zusätzliche Logik auf die Gruppen anwenden können, nachdem Sie sie erstellt haben, indem Sie eine *Fortsetzung* mit `into` verwenden.  Weitere Informationen finden Sie unter [into](../../../csharp/language-reference/keywords/into.md).  Im folgenden Beispiel wird jede Gruppe abgefragt, um nur jene auszuwählen, deren Schlüsselwert ein Vokal ist.  
  
 [!CODE [cscsrefQueryKeywords#17](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#17)]  
  
## Hinweise  
 Zum Zeitpunkt der Kompilierung werden `group`\-Klauseln in Aufrufe der <xref:System.Linq.Enumerable.GroupBy%2A>\-Methode übersetzt.  
  
## Siehe auch  
 <xref:System.Linq.IGrouping%602>   
 <xref:System.Linq.Enumerable.GroupBy%2A>   
 <xref:System.Linq.Enumerable.ThenBy%2A>   
 <xref:System.Linq.Enumerable.ThenByDescending%2A>   
 [Abfrageschlüsselwörter \(LINQ\)](../../../csharp/language-reference/keywords/query-keywords.md)   
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [Gewusst wie: Erstellen einer geschachtelten Gruppe](../../../csharp/programming-guide/linq-query-expressions/how-to-create-a-nested-group.md)   
 [Gewusst wie: Gruppieren von Abfrageergebnissen](../../../csharp/programming-guide/linq-query-expressions/how-to-group-query-results.md)   
 [Gewusst wie: Ausführen einer Unterabfrage für eine Gruppierungsoperation](../../../csharp/programming-guide/linq-query-expressions/how-to-perform-a-subquery-on-a-grouping-operation.md)