---
title: "Visual Basic Features That Support LINQ | Microsoft Docs"
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
  - "Visual Basic, LINQ features"
  - "LINQ [Visual Basic], features supporting LINQ"
ms.assetid: c821bb50-b6f6-4cf9-8aba-2717e465bd3a
caps.latest.revision: 51
caps.handback.revision: 49
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Visual Basic Features That Support LINQ
Der Begriff [!INCLUDE[vbteclinqext](../../../../csharp/getting-started/includes/vbteclinqext_md.md)] bezieht sich auf eine Technologie in Visual Basic, die Abfragesyntax und andere Sprachkonstrukte direkt in der Programmiersprache unterstützt.  Bei [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)] ist es nicht erforderlich, eine neue Programmiersprache zu erlernen, um Abfragen gegen eine externe Datenquelle auszuführen.  Sie können Daten in relationalen Datenbanken, XML\-Speichern oder Objekten mithilfe von Visual Basic abfragen.  Diese Integration von Abfragefunktionen in die Programmiersprache ermöglicht die Suche nach Syntaxfehlern zur Kompilierzeit und bietet Typsicherheit.  Außerdem wird durch diese Integration sichergestellt, dass Ihnen die meisten Informationen, die Sie zum Schreiben umfangreicher, vielseitiger Abfragen in Visual Basic benötigen, bereits bekannt sind.  
  
 In den folgenden Abschnitten werden die neuen Sprachkonstrukte beschrieben, die LINQ unterstützten, um Ihnen den Einstieg in die einführende Dokumentation sowie in Codebeispiele und Beispielanwendungen zu erleichtern.  Sie können auch auf die Links klicken, um genau zu erfahren, wie die Sprachfeatures zur Unterstützung der sprachintegrierten Abfrage \(Language\-Integrated Query, LINQ\) zusammenspielen.  [Exemplarische Vorgehensweise: Schreiben von Abfragen in Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/walkthrough-writing-queries.md) bietet einen guten Einstiegspunkt.  
  
## Abfrageausdrücke  
 Abfrageausdrücke in Visual Basic können ähnlich wie in SQL oder XQuery in einer deklarativen Syntax ausgedrückt werden.  Eine Abfragesyntax wird zur Kompilierzeit in Methodenaufrufe für eine LINQ\-Anbieterimplementierung der standardmäßigen Abfrageoperator\-Erweiterungsmethoden umgewandelt.  Anwendungen steuern, welche Standardabfrageoperatoren sich innerhalb des Bereichs befinden, indem der entsprechende Namespace mit einer `Imports`\-Anweisung angegeben wird.  Die Syntax für einen Visual Basic\-Abfrageausdruck sieht wie folgt aus:  
  
 [!CODE [VbLINQVbFeatures#1](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#1)]  
  
 Weitere Informationen hierzu finden Sie unter [Introduction to LINQ in Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md).  
  
## Implizit typisierte Variablen  
 Anstatt beim Deklarieren und Initialisieren einer Variablen einen Typ explizit anzugeben, können Sie den Compiler zum Ableiten und Zuweisen des Typs veranlassen.  Dies wird als *lokaler Typrückschluss* bezeichnet.  
  
 Variables mit abgeleiteten Typen sind ebenso wie Variablen, deren Typ explizit angegeben wird, stark typisiert.  Der lokale Typrückschluss funktioniert nur, wenn Sie in einem Methodentext eine lokale Variable definieren.  Weitere Informationen finden Sie unter [Option Infer Statement](../../../../visual-basic/language-reference/statements/option-infer-statement.md) und [Local Type Inference](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).  
  
 Im folgenden Beispiel wird der lokalen Typrückschluss veranschaulicht.  Um dieses Beispiel zu verwenden, müssen Sie `Option Infer` auf `On` festlegen.  
  
 [!CODE [VbLINQVbFeatures#2](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#2)]  
  
 Lokaler Typrückschluss ist es auch möglich, dass anonyme Typen zu erstellen, die weiter unten in diesem Abschnitt beschrieben werden, und für LINQ\-Abfragen erforderlich sind.  
  
 Im folgenden LINQ\-Beispiel erfolgt ein Typrückschluss, wenn `Option Infer` den Wert `On` oder `Off` aufweist.  Wenn `Option Infer` gleich `Off` und `Option Strict` gleich `On` ist, tritt ein Kompilierungsfehler auf.  
  
 [!CODE [VbLINQVbFeatures#3](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#3)]  
  
## Objektinitialisierer  
 Objektinitialisierer werden in Abfrageausdrücken verwendet, wenn ein anonymer Typ für die Aufnahme der Ergebnisse einer Abfrage erstellt werden muss.  Sie können auch verwendet werden, um Objekte benannter Typen außerhalb von Abfragen zu initialisieren.  Mit einem Objektinitialisierer können Sie ein Objekt in einer einzelnen Zeile initialisieren, ohne einen Konstruktor explizit aufzurufen.  Beispiel: Bei einer Klasse mit dem Namen `Customer`, die neben anderen Eigenschaften über die öffentliche `Name`\-Eigenschaft und die öffentliche `Phone`\-Eigenschaft verfügt, kann der Objektinitialisierer auf folgende Weise verwendet werden:  
  
 [!CODE [VbLINQVbFeatures#4](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#4)]  
  
 Weitere Informationen finden Sie unter [Object Initializers: Named and Anonymous Types](../../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md).  
  
## Anonyme Typen  
 Mit anonymen Typen können Eigenschaftensätze auf praktische Weise vorübergehend in einem Element gruppiert werden, das Sie in ein Abfrageergebnis aufnehmen möchten.  Auf diese Weise können Sie eine beliebige Kombination verfügbarer Felder in beliebiger Reihenfolge in der Abfrage auswählen, ohne einen benannten Datentyp für das Element zu definieren.  
  
 Ein *anonymer Typ* wird dynamisch vom Compiler erstellt.  Der Name des Typs wird vom Compiler zugewiesen und kann sich bei jeder neuen Kompilierung ändern.  Deshalb kann der Name nicht direkt verwendet werden.  Anonyme Typen werden auf folgende Weise initialisiert:  
  
 [!CODE [VbLINQVbFeatures#5](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#5)]  
  
 Weitere Informationen finden Sie unter [Anonymous Types](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
  
## Erweiterungsmethoden  
 Mit Erweiterungsmethoden können Sie einem Datentyp oder einer Schnittstelle Methoden außerhalb der Definition hinzufügen.  Dieses Feature ermöglicht Ihnen im Prinzip, einem vorhandenen Typ neue Methoden hinzuzufügen, ohne den Typ tatsächlich zu ändern.  Die Standardabfrageoperatoren selbst stellen eine Reihe von Erweiterungsmethoden dar, die [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)]\-Abfragefunktionen für jeden Typ bieten, der <xref:System.Collections.Generic.IEnumerable%601> implementiert. Andere Erweiterungen für <xref:System.Collections.Generic.IEnumerable%601> umfassen <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.Union%2A> und <xref:System.Linq.Enumerable.Intersect%2A>.  
  
 Durch die folgende Erweiterungsmethode wird der <xref:System.String>\-Klasse eine Print\-Methode hinzugefügt.  
  
 [!CODE [VbLINQVbFeatures#6](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#6)]  
  
 Die Methode wird wie jede normale Instanzenmethode von <xref:System.String> aufgerufen:  
  
 [!CODE [VbLINQVbFeatures#7](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#7)]  
  
 Weitere Informationen finden Sie unter [Erweiterungsmethoden](../../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md).  
  
## Lambda\-Ausdrücke  
 Ein Lambda\-Ausdruck ist eine Funktion ohne Namen, von der ein einzelner Wert berechnet und zurückgegeben wird.  Im Gegensatz zu benannten Funktionen kann ein Lambda\-Ausdruck gleichzeitig definiert und ausgeführt werden.  Im folgenden Beispiel wird 4 angezeigt.  
  
 [!CODE [VbLINQVbFeatures#8](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#8)]  
  
 Sie können die Definition des Lambda\-Ausdrucks einem Variablennamen zuweisen und die Funktion anschließend mithilfe des Namens aufrufen.  Im folgenden Beispiel wird ebenfalls 4 angezeigt.  
  
 [!CODE [VbLINQVbFeatures#12](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#12)]  
  
 In [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)] liegen vielen der Standardabfrageoperatoren Lambda\-Ausdrücke zugrunde.  Lambda\-Ausdrücke werden vom Compiler erstellt, um Berechnungen zu erfassen, die in grundlegenden Abfragemethoden wie `Where`, `Select`, `Order By`, `Take While` usw. definiert sind.  
  
 Im folgenden Code wird beispielsweise eine Abfrage definiert, die aus einer Liste von Studenten alle Studenten im Abschlussjahr zurückgibt.  
  
 [!CODE [VbLINQVbFeatures#9](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#9)]  
  
 Die Abfragedefinition wird in mit dem folgenden Beispiel vergleichbaren Code kompiliert, in dem zwei Lambda\-Ausdrücke verwendet werden, um die Argumente für `Where` und `Select` anzugeben.  
  
 [!CODE [VbLINQVbFeatures#10](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#10)]  
  
 Beide Versionen können unter Verwendung einer `For Each`\-Schleife ausgeführt werden:  
  
 [!CODE [VbLINQVbFeatures#11](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQVbFeatures#11)]  
  
 Weitere Informationen finden Sie unter [Lambda Expressions](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).  
  
## Siehe auch  
 [LINQ \(Language\-Integrated Query\)](../Topic/LINQ%20\(Language-Integrated%20Query\).md)   
 [Getting Started with LINQ in Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/getting-started-with-linq.md)   
 [LINQ und Zeichenfolgen](../../../../visual-basic/programming-guide/concepts/linq/linq-and-strings.md)   
 [C\# Features That Support LINQ](../../../../csharp/programming-guide/concepts/linq/features-that-support-linq.md)   
 [Option Infer Statement](../../../../visual-basic/language-reference/statements/option-infer-statement.md)   
 [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)