---
title: "String Basics in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "strings [Visual Basic], Like operator"
  - "strings [Visual Basic], Visual Basic"
  - "strings [Visual Basic], regular expressions"
ms.assetid: 5674418d-f00d-4f72-9f98-d15897793350
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# String Basics in Visual Basic
Der `String`\-Datentyp stellt eine Reihe von Zeichen dar \(wobei jedes Zeichen wiederum eine Instanz des `Char`\-Datentyps darstellt\).  In diesem Thema werden die grundlegenden Konzepte von Zeichenfolgen in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] erläutert.  
  
## Zeichenfolgenvariablen  
 Einer Instanz einer Zeichenfolge kann ein Literalwert zugewiesen werden, der eine Reihe von Zeichen darstellt.  Zum Beispiel:  
  
 [!CODE [VbVbalrStrings#63](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#63)]  
  
 Eine `String`\-Variable kann auch einen beliebigen Ausdruck annehmen, der eine Zeichenfolge ergibt.  Beispiele werden unten gezeigt:  
  
 [!CODE [VbVbalrStrings#64](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#64)]  
  
 Jedes Literal, das einer `String`\-Variable zugewiesen ist, muss in Anführungszeichen eingeschlossen werden \(„“\).  Dies bedeutet, dass ein Anführungszeichen in einer Zeichenfolge nicht durch ein Anführungszeichen dargestellt werden kann.  Beispielsweise verursacht der folgende Code einen Compilerfehler:  
  
 [!CODE [VbVbalrStrings#65](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#65)]  
  
 Dieser Code verursacht einen Fehler, da der Compiler die Zeichenfolge nach dem zweiten Anführungszeichen beendet, und der Rest der Zeichenfolge wird als Code interpretiert.  Zur Lösung dieses Problems interpretiert [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] zwei Anführungszeichen in einem Zeichenfolgenliteral als ein Anführungszeichen in der Zeichenfolge.  Das folgende Beispiel zeigt die korrekte Methode zum Einschließen eines Anführungszeichens in eine Zeichenfolge:  
  
 [!CODE [VbVbalrStrings#66](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#66)]  
  
 Im vorherigen Beispiel werden die beiden Anführungszeichen, die vor dem Wort `Look` vorhanden sind, zu einem Anführungszeichen in der Zeichenfolge.  Die drei Anführungszeichen am Ende der Zeile stellen ein Anführungszeichen in der Zeichenfolge und das Abschlusszeichen der Zeichenfolge dar.  
  
 Zeichenfolgenliterale können mehrere Zeilen enthalten:  
  
```vb  
Dim x = "hello  
world"  
  
```  
  
 Die resultierende Zeichenfolge enthält Zeilenumbruchsequenzen, die Sie in Ihrem Zeichenfolgenliteral \(vbcr, vbcrlf usw.\) verwendet haben.  Sie müssen nicht mehr die bisherige Problemumgehung verwenden:  
  
```vb  
Dim x = <xml><![CDATA[Hello  
World]]></xml>.Value  
  
```  
  
## Zeichen in Zeichenfolgen  
 Eine Zeichenfolge kann als eine Reihe von `Char`\-Werten betrachtet werden, und der `String`\-Typ verfügt über integrierte Funktionen, mit denen Sie zahlreiche Bearbeitungen an einer Zeichenfolge vornehmen können, die den durch Arrays zulässigen Bearbeitungen ähneln.  Wie bei allen Arrays in [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)], handelt es sich dabei um nullbasierte Arrays.  Sie möchten möglicherweise auf ein bestimmtes Zeichen in einer Zeichenfolge durch die `Chars`\-Eigenschaft verweisen, die eine Möglichkeit bietet, auf ein Zeichen durch die Position zuzugreifen, in der es in der Zeichenfolge auftritt.  Zum Beispiel:  
  
 [!CODE [VbVbalrStrings#67](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#67)]  
  
 Im obigen Beispiel gibt die `Chars`\-Eigenschaft der Zeichenfolge das vierte Zeichen in der Zeichenfolge zurück, wobei es sich um `D` handelt, und weist dieses `myChar` zu.  Sie können auch die Länge einer bestimmten Zeichenfolge durch die `Length`\-Eigenschaft abrufen.  Wenn Sie mehrere Bearbeitungen hinsichtlich des Arraytyps an einer Zeichenfolge durchführen müssen, können Sie sie in ein Array von `Char`\-Instanzen mit der `ToCharArray`\-Funktion der Zeichenfolge konvertieren.  Zum Beispiel:  
  
 [!CODE [VbVbalrStrings#68](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#68)]  
  
 Die Variable `myArray` enthält jetzt ein Array von `Char`\-Werten, die jeweils ein Zeichen aus `myString` darstellen.  
  
## Die Unveränderlichkeit von Zeichenfolgen  
 Eine Zeichenfolge ist *unveränderlich*, was bedeutet, dass der entsprechende Wert nicht geändert werden kann, wenn dieser erstellt wurde.  Sie können einer Zeichenfolgenvariablen trotzdem mehr als einen Wert zuweisen.  Betrachten Sie das folgende Beispiel:  
  
 [!CODE [VbVbalrStrings#69](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#69)]  
  
 Hier wird eine Zeichenfolgenvariable erstellt, ein Wert zugewiesen, und dann wird der Wert geändert.  
  
 Genauer gesagt wird in der ersten Zeile eine Instanz des Typs `String` erstellt und der Wert `This string is immutable` zugewiesen.  In der zweiten Zeile des Beispiels wird eine neue Instanz erstellt und der Wert `Or is it?` zugewiesen. Die Zeichenfolgenvariable verwirft den Verweis auf die erste Instanz und speichert einen Verweis auf die neue Instanz.  
  
 Im Gegensatz zu anderen systeminternen Datentypen ist `String` ein Verweistyp.  Wenn eine Variable des Verweistyps als Argument an eine Funktion oder Unterroutine übergeben wird, wird ein Verweis auf die Speicheradresse, wo die Daten gespeichert werden, anstelle des tatsächlichen Werts der Zeichenfolge übergeben.  Damit bleibt der Name der Variable im vorherigen Beispiel gleich, aber es wird auf eine neue und andere Instanz der `String`\-Klasse verwiesen, die den neuen Wert enthält.  
  
## Siehe auch  
 [Introduction to Strings in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)   
 [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md)   
 [Char Data Type](../../../../visual-basic/language-reference/data-types/char-data-type.md)   
 [Grundlegende Zeichenfolgenoperationen](../Topic/Basic%20String%20Operations%20in%20the%20.NET%20Framework.md)