---
title: "Type Relationships in LINQ Query Operations (C#) | Microsoft Docs"
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
  - "inferring type information [LINQ in C#]"
  - "data sources [LINQ in C#], type relationships"
  - "queries [LINQ in C#], type relationships"
  - "relationships [LINQ in C#]"
  - "type relationships [LINQ in C#]"
  - "variable relationships [LINQ in C#]"
  - "type information inferred [LINQ in C#]"
  - "data transformations [LINQ in C#]"
  - "LINQ [C#], type relationships"
ms.assetid: 99118938-d47c-4d7e-bb22-2657a9f95268
caps.latest.revision: 25
caps.handback.revision: 23
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Type Relationships in LINQ Query Operations (C#)
Um Abfragen effektiv erstellen zu können, ist es wichtig, dass Sie verstehen, wie die Variablentypen in einer vollständigen Abfrageoperation miteinander zusammenhängen.  Wenn Sie diese Beziehungen verstehen, können Sie die [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)]\-Beispiele und die Codebeispiele in der Dokumentation besser nachvollziehen.  Weiterhin können Sie dann besser verstehen, was im Hintergrund abläuft, wenn Variablen implizit mithilfe von `var` typisiert werden.  
  
 [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)]\-Abfrageoperationen sind in der Datenquelle, in der Abfrage selbst und in der Abfrageausführung stark typisiert.  Die Variablentypen in der Abfrage müssen mit den Elementtypen in der Datenquelle und mit dem Typ der Iterationsvariablen in der `foreach`\-Anweisung kompatibel sein.  Diese starke Typisierung stellt sicher, dass Typfehler zur Kompilierzeit abgefangen werden, sodass sie korrigiert werden können, bevor die Benutzer sie ausführen.  
  
 Um diese Typbeziehungen zu veranschaulichen, wird in den meisten folgenden Beispielen explizite Typisierung für alle Variablen angewendet.  Im letzten Beispiel wird gezeigt, wie diese Prinzipien auch dann gelten, wenn Sie die implizite Typisierung mithilfe von [var](../../../../csharp/language-reference/keywords/var.md) verwenden.  
  
## Abfragen, bei denen die Quelldaten nicht transformiert werden  
 Die folgende Abbildung zeigt eine [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)]\-Abfrageoperation für Objekte, die keine Transformationen der Daten ausführt.  Die Quelle enthält eine Sequenz von Zeichenfolgen, und die Abfrageausgabe ist ebenfalls eine Sequenz von Zeichenfolgen.  
  
 ![Beziehung von Datentypen in einer LINQ&#45;Abfrage](../../../../csharp/programming-guide/concepts/linq/media/linq_flow1.png "LINQ\_flow1")  
  
1.  Das Typargument der Datenquelle bestimmt den Typ der Bereichsvariablen.  
  
2.  Der Typ des Objekts, das ausgewählt ist, bestimmt den Typ der Abfragevariablen.  In diesem Beispiel ist `name` eine Zeichenfolge.  Daher ist die Abfragevariable eine `IEnumerable`\<Zeichenfolge\>.  
  
3.  Die Abfragevariable durchläuft in der `foreach`\-Anweisung verschiedene Iterationen.  Da die Abfragevariable eine Sequenz von Zeichenfolgen ist, ist die Iterationsvariable ebenfalls eine Zeichenfolge.  
  
## Abfragen, bei denen die Quelldaten transformiert werden  
 Die folgende Abbildung zeigt eine [!INCLUDE[vbtecdlinq](../../../../csharp/includes/vbtecdlinq_md.md)]\-Abfrageoperation, die eine einfache Datentransformation ausführt.  Die Abfrage verwendet eine Sequenz von `Customer`\-Objekten als Eingabe und wählt nur die `Name`\-Eigenschaft im Ergebnis aus.  Da `Name` eine Zeichenfolge ist, erzeugt die Abfrage eine Sequenz von Zeichenfolgen als Ausgabe.  
  
 ![Eine Abfrage, die den Datentyp transformiert](../../../../csharp/programming-guide/concepts/linq/media/linq_flow2.png "LINQ\_flow2")  
  
1.  Das Typargument der Datenquelle bestimmt den Typ der Bereichsvariablen.  
  
2.  Die `select`\-Anweisung gibt die `Name`\-Eigenschaft statt des vollständigen `Customer`\-Objekts zurück.  Da `Name` eine Zeichenfolge ist, lautet das Typargument von `custNameQuery` nicht `Customer`, sondern `string`.  
  
3.  Da `custNameQuery` eine Sequenz von Zeichenfolgen ist, muss die Iterationsvariable der `foreach`\-Schleife auch ein `string` sein.  
  
 Die folgende Abbildung zeigt eine etwas komplexere Transformation.  Die `select`\-Anweisung gibt einen anonymen Typ zurück, der nur zwei Member des ursprünglichen `Customer`\-Objekts erfasst.  
  
 ![Eine Abfrage, die den Datentyp transformiert](../../../../csharp/programming-guide/concepts/linq/media/linq_flow3.png "LINQ\_flow3")  
  
1.  Das Typargument der Datenquelle ist immer der Typ der Bereichsvariablen in der Abfrage.  
  
2.  Da die `select`\-Anweisung einen anonymen Typ erzeugt, muss die Abfragevariable mithilfe von `var` implizit typisiert werden.  
  
3.  Da der Typ der Abfragevariablen implizit ist, muss die Iterationsvariable in der `foreach`\-Schleife auch implizit sein.  
  
## Ableiten von Typinformationen durch den Compiler  
 Auch wenn Sie die Typbeziehungen einer Abfrageoperation grundsätzlich verstehen sollten, haben Sie die Option, den Compiler alle Arbeitsschritte ausführen zu lassen.  Das [var](../../../../csharp/language-reference/keywords/var.md)\-Schlüsselwort kann in einer Abfrageoperation für jede lokale Variable verwendet werden.  Die folgende Abbildung ähnelt Beispiel Nummer 2, das zuvor erläutert wurde.  Allerdings stellt der Compiler den starken Typ für jede Variable in der Abfrageoperation bereit.  
  
 ![Typfluss mit implizierter Typisierung](../../../../csharp/programming-guide/concepts/linq/media/linq_flow4.png "LINQ\_flow4")  
  
 Weitere Informationen über `var` finden Sie unter [Implizit typisierte lokale Variablen](../../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md).  
  
## Siehe auch  
 [Getting Started with LINQ in C\#](../../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md)   
 [Type Relationships in Query Operations \(Visual Basic\)](../../../../visual-basic/programming-guide/concepts/linq/type-relationships-in-query-operations.md)