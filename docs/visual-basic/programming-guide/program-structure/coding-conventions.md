---
title: "Visual Basic Coding Conventions | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "coding conventions, Visual Basic"
  - "examples [Visual Basic], coding conventions"
  - "Visual Basic code, conventions"
ms.assetid: c1df130b-fec6-49a5-becf-0a7e494a1d0f
caps.latest.revision: 48
caps.handback.revision: 48
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Visual Basic Coding Conventions
Microsoft entwickelt Beispiele und Dokumentation, die den Richtlinien in diesem Thema folgen.  Wenn Sie dieselben Codierungskonventionen beachten, erhalten Sie möglicherweise folgende Vorteile:  
  
-   Der Code erhält eine konsistente Gestaltung, damit sich die Leser mehr auf den Inhalt und nicht auf das Layout konzentrieren.  
  
-   Leser verstehen den Code schneller, da sie Rückschlüsse aus früheren Erfahrungen ziehen können.  
  
-   Sie können den Code kopieren, ändern und leichter pflegen.  
  
-   Sie können sicherstellen, dass der Code die "empfohlenen Vorgehensweisen" für Visual Basic berücksichtigt.  
  
## Namenskonventionen  
  
-   Informationen zu Benennungsrichtlinien finden Sie im Thema [Richtlinien für die Benennung](../Topic/Naming%20Guidelines.md).  
  
-   Verwenden Sie nicht "My" oder "my" als Teil eines Variablennamens.  Diese Vorgehensweise führt zu Verwechslungen mit den `My`\-Objekten.  
  
-   Sie müssen die Namen von Objekten in automatisch generiertem Code nicht ändern, um sie an die Richtlinien anzupassen.  
  
## Layoutkonventionen  
  
-   Fügen Sie Registerkarten als Leerzeichen ein, und verwenden Sie intelligenten Einzug mit vier Leerzeichen.  
  
-   Verwenden Sie **Automatische Strukturierung und Einrückung des Programmcodes**, um den Code im Code\-Editor neu zu formatieren.  Weitere Informationen finden Sie unter [Optionen, Text\-Editor, Standard \(Visual Basic\)](/visual-studio/ide/reference/options-text-editor-basic-visual-basic).  
  
-   Verwenden Sie pro Zeile nur eine Anweisung.  Verwenden Sie nicht das Visual Basic\-Zeilentrennzeichen \(:\).  
  
-   Vermeiden Sie, das explizite Zeilenfortsetzungszeichen "\_" zugunsten der impliziten Zeilenfortsetzung, wenn die Sprache dies ermöglicht.  
  
-   Verwenden Sie pro Zeile nur eine Deklaration.  
  
-   Mit **Automatische Strukturierung und Einrückung des Programmcodes** werden Fortsetzungszeilen nicht automatisch formatiert. Sie müssen zum Einrücken manuell auf einen Tabstopp gezogen werden.  In einer Liste werden jedoch die Elemente immer links ausgerichtet.  
  
    ```  
    a As Integer,  
    b As Integer  
    ```  
  
-   Fügen Sie zwischen Methoden\- und Eigenschaftendefinitionen mindestens eine Leerzeile ein.  
  
## Konventionen für Kommentare  
  
-   Fügen Sie den Kommentar in einer eigenen Zeile und nicht am Ende einer Codezeile ein.  
  
-   Beginnen Sie den Kommentartext mit einem Großbuchstaben, und beenden Sie ihn mit einem Punkt.  
  
-   Fügen Sie ein Leerzeichen zwischen dem Kommentartrennzeichen \('\) und dem Kommentartext ein.  
  
     [!CODE [VbVbalrGuidelines#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#2)]  
  
-   Erstellen Sie keine formatierten Blöcke von Sternchen, die die Kommentare umgeben.  
  
## Programmstruktur  
  
-   Wenn Sie die `Main`\-Methode verwenden, verwenden Sie das Standardkonstrukt für neue Konsolenanwendungen, und verwenden Sie `My` für Befehlszeilenargumente.  
  
     [!CODE [VbVbalrGuidelines#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#3)]  
  
## Sprachrichtlinien  
  
### String\-Datentyp  
  
-   Um Zeichenfolgen verketten, verwenden Sie ein kaufmännisches Und\-Zeichen \(&\).  
  
     [!CODE [VbVbalrGuidelines#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#4)]  
  
-   Verwenden Sie das <xref:System.Text.StringBuilder>\-Objekt, um Zeichenfolgen in Schleifen anzuhängen.  
  
     [!CODE [VbVbalrGuidelines#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#5)]  
  
### Weniger strenge Delegaten in Ereignishandlern  
 Um Ereignishandler zu vermeiden, qualifizieren Sie die Argumente \(Object und EventArgs\) nicht explizit.  Wenn Sie nicht die Ereignisargumente verwenden, die an ein Ereignis übergeben werden \(z. B. Sender als Objekt, "e" als EventArgs\), verwenden Sie weniger strenge Delegaten, und lassen Sie die Ereignisargumente im Code aus:  
  
 [!CODE [VbVbalrGuidelines#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#7)]  
  
### Datentyp ohne Vorzeichen  
  
-   Verwenden Sie `Integer` anstelle von Typen ohne Vorzeichen, wenn sie nicht notwendig sind.  
  
### Arrays  
  
-   Verwenden Sie die kurze Syntax, wenn Sie Arrays in der Deklarationszeile initialisieren.  Sie können z. B. folgende Syntax verwenden.  
  
     [!CODE [VbVbalrGuidelines#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#8)]  
  
     Verwenden Sie nicht die folgende Syntax.  
  
     [!CODE [VbVbalrGuidelines#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#9)]  
  
-   Legen Sie den Arraybezeichner im Typ und nicht in der Variablen ab.  Sie können z. B. folgende Syntax verwenden:  
  
     [!CODE [VbVbalrGuidelines#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#11)]  
  
     Verwenden Sie nicht die folgende Syntax:  
  
     [!CODE [VbVbalrGuidelines#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#10)]  
  
-   Verwenden Sie die { }\-Syntax, wenn Sie Arrays aus grundlegenden Datentypen deklarieren und initialisieren.  Sie können z. B. folgende Syntax verwenden:  
  
     [!CODE [VbVbalrGuidelines#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#12)]  
  
     Verwenden Sie nicht die folgende Syntax:  
  
     [!CODE [VbVbalrGuidelines#13](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#13)]  
  
### Verwenden des with\-Schlüsselworts  
 Wenn Sie eine Reihe von Aufrufen eines Objekts ausführen, sollten Sie erwägen, das `With`\-Schlüsselwort zu verwenden:  
  
 [!CODE [VbVbalrGuidelines#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#15)]  
  
### Verwenden Sie try\-catch\-Anweisungen zur Ausnahmebehandlung.  
 Verwenden Sie nicht `On Error Goto`.  
  
### Verwenden des IsNot\-Schlüsselworts  
 Verwenden Sie das Schlüsselwort `IsNot` statt `Not...Is Nothing`.  
  
### New\-Schlüsselwort  
  
-   Verwenden Sie die kurze Instanziierung.  Sie können z. B. folgende Syntax verwenden:  
  
     [!CODE [VbVbalrGuidelines#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#21)]  
  
     Die vorangehende Zeile entspricht der Folgenden:  
  
     [!CODE [VbVbalrGuidelines#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#22)]  
  
-   Verwenden Sie für neue Objekte Objektinitialisierer anstelle des parameterlosen Konstruktors:  
  
     [!CODE [VbVbalrGuidelines#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#23)]  
  
### Ereignisbehandlung  
  
-   Verwenden Sie eher `Handles` als `AddHandler`:  
  
     [!CODE [VbVbalrGuidelines#24](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#24)]  
  
-   Verwenden Sie `AddressOf`, und instanziieren Sie den Delegaten nicht explizit:  
  
     [!CODE [VbVbalrGuidelines#25](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#25)]  
  
-   Wenn Sie ein Ereignis definieren, verwenden Sie die kurze Syntax, und lassen Sie den Delegaten vom Compiler definieren:  
  
     [!CODE [VbVbalrGuidelines#26](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#26)]  
  
-   Überprüfen Sie nicht, ob ein Ereignis `Nothing` \(NULL\) ist, bevor Sie die `RaiseEvent`\-Methode aufrufen.  Die `RaiseEvent`\-Methode führt vor dem Auslösen des Ereignisses eine Überprüfung auf den Wert `Nothing` durch.  
  
### Verwenden von Shared\-Membern  
 Rufen Sie `Shared`\-Member über den Klassennamen auf, nicht von einer Instanzvariablen aus.  
  
### Verwenden von XML\-Literalen  
 XML\-Literale vereinfachen allgemeine Aufgaben bei der Arbeit mit XML \(z. B. Laden, Abfragen und Umwandeln\).  Beachten Sie bei der Entwicklung mit XML die folgenden Richtlinien:  
  
-   Verwenden Sie zum Erstellen von XML\-Dokumenten und –Fragmenten XML\-Literale, anstatt die XML\-APIs direkt aufzurufen.  
  
-   Importieren Sie XML\-Namespaces auf Datei\- oder Projektebene, um die Leistungsoptimierung für XML\-Literale zu verwenden.  
  
-   Verwenden Sie die XML\-Achseneigenschaften, um auf Elemente und Attribute in einem XML\-Dokument zuzugreifen.  
  
-   Verwenden Sie eingebettete Ausdrücke, um Werte einzuschließen und XML aus vorhandenen Werten zu erstellen, anstatt API\-Aufrufe wie die `Add`\-Methode zu nutzen:  
  
     [!CODE [VbVbalrGuidelines#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#27)]  
  
### LINQ\-Abfragen  
  
-   Verwenden Sie aussagekräftige Namen für Abfragevariablen:  
  
     [!CODE [VbVbalrGuidelines#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#28)]  
  
-   Geben Sie Aliasnamen für Elemente in einer Abfrage an, um eine korrekte Großschreibung von Eigenschaftennamen anonymer Typen in Pascal\-Schreibweise sicherzustellen:  
  
     [!CODE [VbVbalrGuidelines#29](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#29)]  
  
-   Benennen Sie Eigenschaften um, wenn die Eigenschaftennamen im Ergebnis nicht eindeutig sind.  Wenn die Abfrage beispielsweise einen Kundennamen und eine Auftrags\-ID zurückgibt, sollten Sie diese im Ergebnis umbenennen, anstatt `Name` und `ID` zu übernehmen:  
  
     [!CODE [VbVbalrGuidelines#30](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#30)]  
  
-   Verwenden Sie den Typrückschluss in der Deklaration von Abfragevariablen und Bereichsvariablen:  
  
     [!CODE [VbVbalrGuidelines#31](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#31)]  
  
-   Richten Sie Abfrageklauseln unter der `From`\-Anweisung aus:  
  
     [!CODE [VbVbalrGuidelines#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#32)]  
  
-   Verwenden Sie vor anderen Abfrageklauseln `Where`\-Klauseln, sodass die nachfolgenden Abfrageklauseln für den reduzierten, gefilterten Datensatz ausgeführt werden:  
  
     [!CODE [VbVbalrGuidelines#33](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#33)]  
  
-   Verwenden Sie zum expliziten Definieren eines Verbindungsvorgangs die `Join`\-Klausel anstelle der `Where`\-Klausel, bei der ein Verbindungsvorgang implizit definiert wird:  
  
     [!CODE [VbVbalrGuidelines#34](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrGuidelines#34)]  
  
## Siehe auch  
 [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md)