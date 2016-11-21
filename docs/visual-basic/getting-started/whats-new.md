---
title: "What&#39;s New for Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "VB.StartPage.WhatsNew"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "new features, Visual Basic"
  - "what's new [Visual Basic]"
  - "Visual Basic, what's new"
ms.assetid: d7e97396-7f42-4873-a81c-4ebcc4b6ca02
caps.latest.revision: 145
caps.handback.revision: 145
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# What&#39;s New for Visual Basic
Auf dieser Seite sind die Namen der wichtigsten Features für jede Version von Visual Basic mit Beschreibungen der neuen und verbesserten Features in der neuesten Version der Sprache aufgelistet.  
  
## Frühere Versionen  
 Visual Basic \/ Visual Studio .NET 2002  
 Erste Version  
  
 Visual Basic \/ Visual Studio .NET 2003  
 Bitschiebeoperatoren, Deklaration von Schleifenvariablen  
  
 Visual Basic \/ Visual Studio .NET 2005  
 `My`\-Typ und Hilfstypen \(Zugriff auf App, Computer, Dateisystem, Netzwerk\)  
  
 Visual Basic \/ Visual Studio .NET 2008  
 Language Integrated Query \(LINQ\), XML\-Literale, lokaler Typrückschluss, Objektinitialisierer, anonyme Typen, Erweiterungsmethoden, lokaler `var`\-Typrückschluss, Lambda\-Ausdrücke, `if`\-Operator, partielle Methoden, auf NULL festlegbare Werttypen  
  
 Visual Basic, Visual Studio .NET 2010  
 Automatisch implementierte Eigenschaften, Auflistungsinitialisierer, implizite Zeilenfortsetzung, dynamische, generische Ko\-\/Kontravarianz, Zugriff auf globalen Namespace  
  
 Visual Basic \/ Visual Studio .NET 2012  
 `Async`\/`await`, Iteratoren, Aufrufer\-Informationsattribute  
  
 Visual Basic \/ Visual Studio .NET 2013  
 Technologievorschau von .NET Compiler Platform \("Roslyn"\)  
  
 Visual Basic \/ Visual Studio .NET 2015  
 Aktuelle Version, siehe unten  
  
## Aktuelle Version  
 [Nameof](../../csharp/language-reference/keywords/nameof.md)  
 Sie können den nicht qualifizierten Zeichenfolgennamen eines Typs oder Members zur Verwendung in einer Fehlermeldung ohne Hartcodierung einer Zeichenfolge abrufen.  Dadurch bleibt der Code bei der Umgestaltung korrekt.  Dieses Feature eignet sich auch zum Einbinden von MVC\-Links \(Model\-View\-Controller\) und das Auslösen von Ereignissen durch geänderte Eigenschaften.  
  
 [Zeichenfolgeninterpolierung](../../csharp/language-reference/keywords/interpolated-strings.md)  
 Sie können Ausdrücke für die Zeichenfolgeninterpolierung zum Erstellen von Zeichenfolgen verwenden.  Ein Ausdruck für eine interpolierte Zeichenfolge sieht wie eine Vorlagenzeichenfolge aus, die Ausdrücke enthält.  C\# erstellt eine Zeichenfolge, indem die Ausdrücke durch die ToString\-Darstellungen der Ergebnisse dieser Ausdrücke ersetzt werden.  Eine interpolierte Zeichenfolge ist in Bezug auf die Argumente leichter zu verstehen als eine [Kombinierte Formatierung](../Topic/Composite%20Formatting.md).  
  
 [Memberzugriff und Indizierung mit NULL\-Bedingung](../../csharp/language-reference/operators/null-conditional-operators.md)  
 Sie können eine Prüfung auf null auf sehr einfache syntaktische Weise vornehmen, bevor Sie eine Operation für den Memberzugriff \(`?.`\) oder die Indizierung \(`?[]`\) ausführen.  Mithilfe dieser Operatoren müssen Sie für die Prüfung auf null weniger Code schreiben, insbesondere beim tieferen Eindringen in Datenstrukturen.  Wenn der linke Operand oder Objektverweis null ist, geben die Operationen null zurück.  
  
 [Mehrzeilige Zeichenfolgenliterale](../../visual-basic/programming-guide/language-features/strings/string-basics.md)  
 Zeichenfolgenliterale können Zeilenumbruchsequenzen enthalten.  Sie müssen nicht mehr die alte Problemumgehung mit `<xml><![CDATA[...text with newlines...]]></xml>.Value` verwenden.  
  
 Kommentare  
 Sie können Kommentare nach impliziten Zeilenfortsetzungen, innerhalb von Initialisierungsausdrücken und zwischen LINQ\-Ausdrücken einfügen.  
  
 Intelligentere Auflösung vollqualifizierter Namen  
 Bei Code wie `Threading.Thread.Sleep(1000)` suchte Visual Basic bisher den Namespace "Threading", stellte fest, dass dieser mit "System.Threading" und "System.Windows.Threading" mehrdeutig war und meldete dann einen Fehler.  Nun berücksichtigt Visual Basic die beiden möglichen Namespaces gemeinsam.  Wenn Sie die Vervollständigungsliste anzeigen, listet der Visual Studio\-Editor Member beider Typen in der Vervollständigungsliste auf.  
  
 Datumsliterale mit Jahresangabe am Anfang  
 Datumsliterale im Format jjjj\-mm\-tt sind möglich, z. B. `#2015-03-17 16:10 PM#`.  
  
 Schreibgeschützte Schnittstelleneigenschaften  
 Sie können mithilfe einer Readwrite\-Eigenschaft schreibgeschützte Schnittstelleneigenschaften implementieren.  Die Schnittstelle garantiert Mindestfunktionalität und hindert eine Implementierungsklasse nicht daran, die Festlegung der Eigenschaft zuzulassen.  
  
 [TypeOf \<expr\> IsNot \<type\>](../../visual-basic/language-reference/operators/typeof-operator.md)  
 Zur besseren Lesbarkeit des Codes können Sie nun `TypeOf` mit `IsNot` verwenden.  
  
 [\#Disable Warning \<ID\> und \#Enable Warning \<ID\>](../../visual-basic/language-reference/directives/directives.md)  
 Sie können bestimmte Warnungen für Bereiche innerhalb einer Quelldatei deaktivieren und aktivieren.  
  
 Verbesserungen bei XML\-Dokumentationskommentaren  
 Beim Schreiben von Dokumentationskommentaren steht intelligente Editor\- und Buildunterstützung zum Überprüfen von Parameternamen, ordnungsgemäßer Handhabung von `crefs` \(Generika, Operatoren usw.\), Farben und Umgestaltung bereit.  
  
 [Partielle Modul\- und Schnittstellendefinitionen](../../visual-basic/language-reference/modifiers/partial.md)  
 Zusätzlich zu Klassen und Strukturen können Sie partielle Module und Schnittstellen deklarieren.  
  
 [\#Region\-Direktiven in Methodentexten](../../visual-basic/language-reference/directives/region-directive.md)  
 Sie können die Begrenzer \#Region...\#End Region an einer beliebigen Stelle in einer Datei, innerhalb von Funktionen und sogar Funktionsrümpfe übergreifend einfügen.  
  
 [Überschreibungsdefinitionen sind implizite Überladungen](../../visual-basic/language-reference/modifiers/overrides.md)  
 Wenn Sie den `Overrides`\-Modifizierer zu einer Definition hinzufügen, fügt der Compiler implizit `Overloads` hinzu, sodass Sie in allgemeinen Fällen weniger Code eingeben können.  
  
 CObj in Attributargumenten zulässig  
 Der Compiler gab gewöhnlich eine Fehlermeldung aus, dass CObj\(...\) bei Verwendung in Attributkonstruktionen keine Konstante war.  
  
 Deklarieren und Verwenden mehrdeutiger Methoden von unterschiedlichen Schnittstellen  
 Zuvor führte der folgende Code zu Fehlern, die Sie daran hinderten, `IMock` zu deklarieren oder `GetDetails` aufzurufen \(wenn diese in C\# deklariert waren\):  
  
```vb  
Interface ICustomer  
  Sub GetDetails(x As Integer)  
End Interface  
  
Interface ITime  
  Sub GetDetails(x As String)  
End Interface  
  
Interface IMock : Inherits ICustomer, ITime  
  Overloads Sub GetDetails(x As Char)  
End Interface  
  
Interface IMock2 : Inherits ICustomer, ITime  
End Interface  
  
```  
  
 Nun verwendet der Compiler normale Regeln zur Überladungsauflösung, um die am besten geeignete `GetDetails`\-Methode zum Aufrufen auszuwählen, und Sie können Schnittstellenbeziehungen in Visual Basic deklarieren, wie sie im Beispiel gezeigt sind.  
  
## Siehe auch  
 [Neues in Visual Studio 2015](/visual-studio/ide/what-s-new-in-visual-studio-2015)