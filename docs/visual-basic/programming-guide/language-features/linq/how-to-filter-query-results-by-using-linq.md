---
title: "How to: Filter Query Results by Using LINQ (Visual Basic) | Microsoft Docs"
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
  - "filtering [Visual Basic]"
  - "filtering data [LINQ in Visual Basic]"
  - "filtering [LINQ in Visual Basic]"
  - "queries [LINQ in Visual Basic], filtering results"
  - "querying databases [LINQ]"
  - "queries [LINQ in Visual Basic], how-to topics"
  - "query samples [Visual Basic]"
  - "filtering data [Visual Basic]"
ms.assetid: ef103092-9bed-4134-97f4-2db696e83c12
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Filter Query Results by Using LINQ (Visual Basic)
Language\-Integrated Query \(LINQ\) vereinfacht den Zugriff auf Datenbankinformationen und das Ausführen von Abfragen.  
  
 Im folgenden Beispiel wird gezeigt, wie eine neue Anwendung erstellt wird, die eine SQL Server\-Datenbank abfragt und die Ergebnisse nach einem bestimmten Wert mithilfe der `Where`\-Klausel filtert.  Weitere Informationen finden Sie unter [Where Clause](../../../../visual-basic/language-reference/queries/where-clause.md).  
  
 In den Beispielen dieses Themas wird die Beispieldatenbank Northwind verwendet.  Wenn die Beispieldatenbank Northwind auf dem Entwicklungscomputer nicht installiert ist, können Sie sie von der Website [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkID=98088) herunterladen.  Anweisungen dazu finden Sie unter [Herunterladen von Beispieldatenbanken](../Topic/Downloading%20Sample%20Databases.md).  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So erstellen Sie eine Verbindung zu einer Datenbank  
  
1.  Öffnen Sie in Visual Studio den **Server\-Explorer**\/**Datenbank\-Explorer**, indem Sie im Menü **Ansicht** auf **Server\-Explorer**\/**Datenbank\-Explorer** klicken.  
  
2.  Klicken Sie im **Server\-Explorer**\/**Datenbank\-Explorer** mit der rechten Maustaste auf **Datenverbindungen** und anschließend auf **Verbindung hinzufügen**.  
  
3.  Geben Sie eine gültige Verbindung zur Beispieldatenbank Northwind an.  
  
### So fügen Sie ein Projekt hinzu, das eine LINQ to SQL\-Datei enthält  
  
1.  Zeigen Sie in Visual Studio im Menü **Datei** auf **Neu**, und klicken Sie auf **Projekt**.  Wählen Sie Visual Basic\-**Windows Forms\-Anwendung** als Projekttyp aus.  
  
2.  Klicken Sie im Menü **Projekt** auf **Neues Element hinzufügen**.  Wählen Sie die Elementvorlage **LINQ to SQL\-Klassen** aus.  
  
3.  Nennen Sie die Datei `northwind.dbml`.  Klicken Sie auf **Hinzufügen**.  Der Object Relational Designer \(O\/R\-Designer\) wird für die Datei northwind.dbml geöffnet.  
  
### So fügen Sie abzufragende Tabellen zum O\/R\-Designer hinzu  
  
1.  Erweitern Sie im **Server\-Explorer**\/**Datenbank\-Explorer** die Verbindung zur Datenbank Northwind.  Erweitern Sie den Ordner **Tabellen**.  
  
     Wenn Sie den O\/R\-Designer geschlossen haben, können Sie ihn durch Doppelklicken auf die zuvor hinzugefügte Datei northwind.dbml erneut öffnen.  
  
2.  Klicken Sie auf die Tabelle Customers, und ziehen Sie sie in den linken Bereich des Designers.  Klicken Sie auf die Tabelle Orders, und ziehen Sie sie in den linken Bereich des Designers.  
  
     Der Designer erstellt neue `Customer`\-Objekte und neue `Order`\-Objekte für das Projekt.  Beachten Sie, dass der Designer Beziehungen zwischen den Tabellen automatisch erkennt und untergeordnete Eigenschaften für verknüpfte Objekte erstellt.  So wird beispielsweise von IntelliSense angezeigt, dass das `Customer`\-Objekt über eine `Orders`\-Eigenschaft für alle Bestellungen dieses Kunden verfügt.  
  
3.  Speichern Sie die Änderungen, und schließen Sie den Designer.  
  
4.  Speichern Sie das Projekt.  
  
### So fügen Sie Code für Datenbankabfragen und zum Anzeigen der Ergebnisse hinzu  
  
1.  Ziehen Sie aus der **Toolbox** ein <xref:System.Windows.Forms.DataGridView>\-Steuerelement auf das Standard\-Windows Form \(Form1\) des Projekts.  
  
2.  Doppelklicken Sie auf Form1, um dem `Load`\-Ereignis des Formulars Code hinzuzufügen.  
  
3.  Wenn Sie dem O\/R\-Designer Tabellen hinzugefügt haben, wurde dem Projekt vom Designer ein <xref:System.Data.Linq.DataContext>\-Objekt hinzugefügt.  Dieses Objekt enthält den Code, der für den Zugriff auf diese Tabellen sowie auf einzelne Objekte und Auflistungen für jede Tabelle benötigt wird.  Das <xref:System.Data.Linq.DataContext>\-Objekt des Projekts wird auf Grundlage des Namens der DBML\-Datei benannt.  Für dieses Projekt lautet der Name des <xref:System.Data.Linq.DataContext>\-Objekts `northwindDataContext`.  
  
     Sie können im Code eine Instanz von <xref:System.Data.Linq.DataContext> erstellen und die vom O\/R\-Designer angegebenen Tabellen abfragen.  
  
     Fügen Sie dem `Load`\-Ereignis folgenden Code hinzu, um die als Eigenschaften des Datenkontexts verfügbar gemachten Tabellen abzufragen.  Die Abfrage filtert die Ergebnisse und gibt nur die Kunden zurück, deren Standort sich in `London` befindet.  
  
     [!CODE [VbLINQToSQLHowTos#11](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos#11)]  
  
4.  Drücken Sie F5, um das Projekt auszuführen und die Ergebnisse anzuzeigen.  
  
5.  Im Folgenden finden Sie einige weitere Filter zum Ausprobieren.  
  
     [!CODE [VbLINQToSQLHowTos#12](../CodeSnippet/VS_Snippets_VBCSharp/VbLINQtoSQLHowTos#12)]  
  
## Siehe auch  
 [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)   
 [Queries](../../../../visual-basic/language-reference/queries/queries.md)   
 [LINQ to SQL](../Topic/LINQ%20to%20SQL.md)   
 [DataContext\-Methoden \(O\/R\-Designer\)](/visual-studio/data-tools/datacontext-methods-o-r-designer)   
 [Exemplarische Vorgehensweise: Erstellen von LINQ to SQL\-Klassen \(O\/R\-Designer\)](../Topic/Walkthrough:%20Creating%20LINQ%20to%20SQL%20Classes%20\(O-R%20Designer\).md)