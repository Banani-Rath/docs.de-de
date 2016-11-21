---
title: "Codekonventionen f&#252;r C# (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "C#-Sprache, Codekonventionen"
  - "Codekonventionen, C#"
  - "Visual C#, Codekonventionen"
ms.assetid: f4f60de9-d49b-4fb6-bab1-20e19ea24710
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Codekonventionen f&#252;r C# (C#-Programmierhandbuch)
Die [C\#\-Sprachspezifikation](http://go.microsoft.com/fwlink/?LinkId=199552) definiert keinen Codierungsstandard.  Die Richtlinien in diesem Thema werden jedoch von Microsoft verwendet, um Beispiele und die Dokumentation zu entwickeln.  
  
 Codierungskonventionen dienen den folgenden Zwecken:  
  
-   Sie kreieren ein konsistentes Erscheinungsbild des Codes, sodass Leser sich auf den Inhalt und nicht auf das Layout konzentrieren können.  
  
-   Sie ermöglichen es den Lesern, Code schneller zu verstehen, da Rückschlüsse basierend auf den bisherigen Erfahrungen gezogen werden können.  
  
-   Sie erleichtern das Kopieren, Ändern und Pflegen des Codes.  
  
-   Sie zeigen die Best Practices für C\#.  
  
## Namenskonventionen  
  
-   Verwenden Sie in kurzen Beispielen, die keine [using\-Direktiven](../../../csharp/language-reference/keywords/using-directive.md) umfassen, Namespacequalifizierungen.  Wenn Sie wissen, dass ein Namespace standardmäßig in ein Projekt importiert wird, müssen Sie den Namen aus diesem Namespace nicht voll qualifizieren.  Qualifizierte Namen können nach einem Punkt \(.\) unterbrochen werden, wenn sie für eine einzelne Zeile zu lang sind, wie im folgenden Beispiel gezeigt.  
  
     [!CODE [csProgGuideCodingConventions#1](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#1)]  
  
-   Sie müssen nicht die Namen der Objekte ändern, die mit den Designertools von Visual Studio erstellt wurden, um sie an andere Richtlinien anzupassen.  
  
## Layoutkonventionen  
 Ein gutes Layout verwendet Formatierungen, um die Struktur des Codes hervorzuheben und um den Code verständlicher zu gestalten.  Microsoft\-Beispiele entsprechen den folgenden Konventionen:  
  
-   Verwenden Sie die Code\-Editor\-Standardeinstellungen \(Intelligenter Einzug, vierstelliger Einzug, als Leerzeichen gespeicherte Tabulatoren\).  Weitere Informationen finden Sie unter [Optionen, Text\-Editor, C\#, Formatierung](/visual-studio/ide/reference/options-text-editor-csharp-formatting)  
  
-   Schreiben Sie pro Zeile nur eine Anweisung.  
  
-   Schreiben Sie pro Zeile nur eine Deklaration.  
  
-   Wenn Fortsetzungszeilen nicht automatisch eingezogen werden, rücken Sie diese um einen Tabstopp \(vier Leerzeichen\) ein.  
  
-   Fügen Sie zwischen Methoden\- und Eigenschaftsdefinitionen mindestens eine Leerzeile ein.  
  
-   Verwenden Sie Klammern, um Klauseln in einem Ausdruck zu kennzeichnen, wie im folgenden Code gezeigt.  
  
     [!CODE [csProgGuideCodingConventions#2](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#2)]  
  
## Konventionen für Kommentare  
  
-   Fügen Sie den Kommentar in einer eigenen Zeile und nicht am Ende einer Codezeile ein.  
  
-   Beginnen Sie Kommentartext mit einem Großbuchstaben.  
  
-   Beenden Sie den Kommentartext mit einem Punkt.  
  
-   Fügen Sie ein Leerzeichen zwischen dem Kommentartrennzeichen \(\/\/\) und dem Kommentartext ein, wie im folgenden Beispiel gezeigt.  
  
     [!CODE [csProgGuideCodingConventions#3](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#3)]  
  
-   Erstellen Sie keine formatierten Blöcke mit Sternchen um Kommentare.  
  
## Sprachrichtlinien  
 In den folgenden Abschnitten werden die Vorgehensweisen beschrieben, denen das C\#\-Team folgt, um Codebeispiele zu erstellen.  
  
### String\-Datentyp  
  
-   Verwenden Sie den `+`\-Operator, um kurze Zeichenfolgen zu verketten, wie im folgenden Code gezeigt.  
  
     [!CODE [csProgGuideCodingConventions#6](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#6)]  
  
-   Verwenden Sie ein <xref:System.Text.StringBuilder>\-Objekt, um Zeichenfolgen in Schleifen anzufügen, besonders bei der Arbeit mit großen Textmengen.  
  
     [!CODE [csProgGuideCodingConventions#7](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#7)]  
  
### Implizit typisierte lokale Variablen  
  
-   Verwenden Sie die [implizite Typisierung](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md) für lokale Variablen, wenn der Typ der Variablen auf der rechten Seite der Zuweisung offensichtlich ist oder wenn der genaue Typ nicht von Bedeutung ist.  
  
     [!CODE [csProgGuideCodingConventions#8](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#8)]  
  
-   Verwenden Sie keine [var](../../../csharp/language-reference/keywords/var.md), wenn der Typ nicht von der rechten Seite der Zuweisung offensichtlich ist.  
  
     [!CODE [csProgGuideCodingConventions#9](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#9)]  
  
-   Verlassen Sie sich nicht auf den Variablennamen, um den Typ der Variable anzugeben.  Er ist unter Umständen nicht korrekt.  
  
     [!CODE [csProgGuideCodingConventions#10](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#10)]  
  
-   Vermeiden Sie den Einsatz von `var` anstelle von [dynamic](../../../csharp/language-reference/keywords/dynamic.md).  
  
-   Verwenden Sie die implizite Typisierung, um den Typ der Schleifenvariablen in [for](../../../csharp/language-reference/keywords/for.md)\- und [foreach](../../../csharp/language-reference/keywords/foreach-in.md)\-Schleifen zu bestimmen.  
  
     Im folgenden Beispiel wird die implizite Typisierung in einer `for`\-Anweisung verwendet.  
  
     [!CODE [csProgGuideCodingConventions#11](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#11)]  
  
     Im folgenden Beispiel wird die implizite Typisierung in einer `foreach`\-Anweisung verwendet.  
  
     [!CODE [csProgGuideCodingConventions#12](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#12)]  
  
### Datentyp ohne Vorzeichen  
  
-   Verwenden Sie im Allgemeinen `int` anstelle von Typen ohne Vorzeichen.  Die Verwendung von `int` ist in C\# üblich; durch den Einsatz von `int` wird die Interaktion mit anderen Bibliotheken vereinfacht.  
  
### Arrays  
  
-   Verwenden Sie die präzise Syntax, wenn Sie Arrays in der Deklarationszeile initialisieren.  
  
     [!CODE [csProgGuideCodingConventions#13](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#13)]  
  
### Delegaten  
  
-   Verwenden Sie die präzise Syntax, um Instanzen eines Delegattyps zu erstellen.  
  
     [!CODE [csProgGuideCodingConventions#14](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#14)]  
  
     [!CODE [csProgGuideCodingConventions#15](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#15)]  
  
### try\-catch\- und using\-Anweisungen in der Ausnahmebehandlung  
  
-   Verwenden Sie eine [try\-catch\-](../../../csharp/language-reference/keywords/try-catch.md)\-Anweisung für die meisten Ausnahmebehandlungen.  
  
     [!CODE [csProgGuideCodingConventions#16](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#16)]  
  
-   Vereinfachen Sie den Code mithilfe der C\#\-Anweisung [using](../../../csharp/language-reference/keywords/using-statement.md).  Verwenden Sie bei einer [try\-finally](../../../csharp/language-reference/keywords/try-finally.md)\-Anweisung, in der der einzige Code im `finally`\-Block ein Aufruf der <xref:System.IDisposable.Dispose%2A>\-Methode ist, stattdessen eine `using`\-Anweisung.  
  
     [!CODE [csProgGuideCodingConventions#17](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#17)]  
  
### &&\- und &#124;&#124;\-Operatoren  
  
-   Um Ausnahmen zu vermeiden und die Leistung zu verbessern, indem Sie unnötige Vergleiche überspringen, verwenden Sie [&&](../../../csharp/language-reference/operators/conditional-and-operator.md) anstelle von [&](../../../csharp/language-reference/operators/and-operator.md) und [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md) anstelle von                                       [&#124;](../../../csharp/language-reference/operators/or-operator.md) , wenn Sie Vergleiche ausführen, wie im folgenden Beispiel gezeigt.  
  
     [!CODE [csProgGuideCodingConventions#18](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#18)]  
  
### New\-Operator  
  
-   Verwenden Sie die präzise Form der Objektinstanziierung mit impliziter Typisierung, wie in der folgenden Deklaration dargestellt.  
  
     [!CODE [csProgGuideCodingConventions#19](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#19)]  
  
     Die vorherige Zeile entspricht der folgenden Deklaration.  
  
     [!CODE [csProgGuideCodingConventions#20](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#20)]  
  
-   Verwenden Sie Objektinitialisierer, um die Objekterstellung zu vereinfachen.  
  
     [!CODE [csProgGuideCodingConventions#21](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#21)]  
  
### Ereignisbehandlung  
  
-   Wenn Sie einen Ereignishandler definieren, den Sie später nicht entfernen müssen, verwenden Sie einen Lambda\-Ausdruck.  
  
     [!CODE [csProgGuideCodingConventions#22](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#22)]  
  
     [!CODE [csProgGuideCodingConventions#23](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#23)]  
  
### Statische Member  
  
-   Rufen Sie [statische](../../../csharp/language-reference/keywords/static.md) Member über den Klassennamen *Klassenname.StatischerMember* auf.  Durch diese Empfehlung ist der Code besser lesbar, da der statische Zugriff eindeutig ist.  Qualifizieren Sie keinen statischen Member, der in einer Basisklasse mit dem Namen einer abgeleiteten Klasse definiert ist.  Während dieser Code kompiliert wird, ist die Lesbarkeit des Codes irreführend, und der Code kann später beschädigt werden, wenn Sie der abgeleiteten Klasse einen statischen Member mit dem gleichen Namen hinzufügen.  
  
### LINQ\-Abfragen  
  
-   Verwenden Sie aussagekräftige Namen für Abfragevariablen.  Im folgenden Beispiel wird `seattleCustomers` für Kunden in Seattle verwendet.  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   Verwenden Sie Aliase, um mithilfe der Pascal\-Schreibweise sicherzustellen, dass die korrekte Großschreibung von Eigenschaftennamen anonymer Typen verwendet wird.  
  
     [!CODE [csProgGuideCodingConventions#26](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#26)]  
  
-   Benennen Sie Eigenschaften um, wenn die Eigenschaftennamen im Ergebnis nicht eindeutig sind.  Wenn die Abfrage beispielsweise einen Kundennamen und eine Händler\-ID zurückgibt, anstatt sie als `Name` und `ID` im Ergebnis beizubehalten, benennen Sie sie um, um zu verdeutlichen, dass `Name` der Name eines Kunden und `ID` die ID eines Händlers ist.  
  
     [!CODE [csProgGuideCodingConventions#27](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#27)]  
  
-   Verwenden Sie die implizierte Typisierung in der Deklaration von Abfragevariablen und Bereichsvariablen.  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   Richten Sie Abfrageklauseln unter der [from](../../../csharp/language-reference/keywords/from-clause.md)\-Klausel aus, wie in den vorherigen Beispielen gezeigt.  
  
-   Verwenden Sie vor anderen Abfrageklauseln [where](../../../csharp/language-reference/keywords/where-clause.md)\-Klauseln, um sicherzustellen, dass nachfolgende Abfrageklauseln für den reduzierten, gefilterten Datensatz ausgeführt werden.  
  
     [!CODE [csProgGuideCodingConventions#29](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#29)]  
  
-   Verwenden Sie mehrere `from`\-Klauseln anstelle von einer [join](../../../csharp/language-reference/keywords/join-clause.md)\-Klausel, um auf die inneren Auflistungen zuzugreifen.  Eine Auflistung von `Student`\-Objekten kann beispielsweise jeweils eine Auflistung von Testergebnissen enthalten.  Wenn die folgende Abfrage ausgeführt wird, wird jedes Ergebnis über 90 zusammen mit dem Nachnamen des Studenten zurückgegeben, der das Testergebnis erzielt hat.  
  
     [!CODE [csProgGuideCodingConventions#30](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#30)]  
  
## Sicherheit  
 Befolgen Sie die Richtlinien in [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md).  
  
## Siehe auch  
 [Visual Basic Coding Conventions](../../../visual-basic/programming-guide/program-structure/coding-conventions.md)   
 [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md)