---
title: "Erstellen von der Befehlszeile aus (Visual Basic) | Microsoft Docs"
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
  - "Builds [Visual Basic], Befehlszeile"
  - "Visual Basic-Compiler, Informationen über Visual Basic-Compiler"
  - "Befehlszeile [Visual Basic], Compiler"
  - "Befehlszeile [Visual Basic], Erstellen über"
  - "Befehlszeile [Visual Basic], Builds"
  - "Compiler, Aufrufen über die Befehlszeile"
  - "Erstellen über die Befehlszeile"
  - "Kompilieren von Quellcode"
  - "Befehlszeilencompiler, Visual Basic"
  - "Befehlszeile [Visual Basic], Visual Basic"
ms.assetid: e61947e9-a42e-4717-a699-5f70a98cdd03
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Erstellen von der Befehlszeile aus (Visual Basic)
Ein [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Projekt besteht aus einer oder mehreren separaten Quelldateien.  Während des als Kompilierung bezeichneten Vorgangs werden diese Dateien zu einem Paket zusammengefasst – einer ausführbaren Datei, die als Anwendung ausgeführt werden kann.  
  
 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] stellt einen Befehlszeilencompiler als Alternative zum Kompilieren von Programmen in der integrierten Entwicklungsumgebung \(IDE\) von [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] bereit.  Der Befehlszeilencompiler bietet sich vor allem dann an, wenn Sie nicht sämtliche Features der IDE benötigen, weil Sie z. B. mit Computern mit begrenztem Systemspeicher oder geringer Speicherkapazität arbeiten oder Programme für solche Computer schreiben.  
  
 Beim Kompilieren von der Befehlszeile aus müssen Sie mit der `/reference`\-Compileroption explizit auf die Laufzeitbibliothek von Microsoft [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] verweisen.  
  
 Um Quelldateien in der [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)]\-IDE zu kompilieren, wählen Sie im Menü **Erstellen** den Befehl **Erstellen** aus.  
  
> [!TIP]
>  Wenn Sie Projektdateien erstellen, indem Sie die Visual Studio\-IDE verwenden, können Sie Informationen zum zugeordneten **vbc** Befehl und seine Schalter im Ausgabefenster anzeigen.  Um diese Informationen anzuzeigen, öffnen Sie [Optionen \(Dialogfeld\), Projekte und Projektmappen, Erstellen und Ausführen](/visual-studio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), und legen Sie dann **Ausführlichkeit der MSBuild\-Projektbuildausgabe** zu **Normal** oder eine höhere Ebene des Ausführlichkeitsgrads fest.  Weitere Informationen finden Sie unter [Gewusst wie: Anzeigen, Speichern und Konfigurieren von Buildprotokolldateien](../Topic/How%20to:%20View,%20Save,%20and%20Configure%20Build%20Log%20Files.md).  
  
 Sie können Dateien des Projekts \(.vbproj\) an einer Eingabeaufforderung kompilieren, indem Sie MSBuild verwenden.  Weitere Informationen finden Sie unter [Command\-Line Reference](/visual-studio/msbuild/msbuild-command-line-reference) und [Walkthrough: Using MSBuild](../Topic/Walkthrough:%20Using%20MSBuild.md).  
  
## In diesem Abschnitt  
 [How to: Invoke the Command\-Line Compiler](../../../visual-basic/reference/command-line-compiler/how-to-invoke-the-command-line-compiler.md)  
 Beschreibt, wie der Befehlszeilencompiler an der MS\-DOS\-Eingabeaufforderung oder von einem bestimmten Unterverzeichnis aus aufgerufen wird.  
  
 [Beispiele für Kompilierungsbefehlszeilen](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 Enthält eine Liste mit Beispielbefehlszeilen, die Sie nach Bedarf abwandeln können.  
  
## Verwandte Abschnitte  
 [Visual Basic Command\-Line Compiler](../../../visual-basic/reference/command-line-compiler/index.md)  
 Enthält Listen mit Compileroptionen, die in alphabetischer Reihenfolge oder nach Zweck angeordnet sind.  
  
 [Conditional Compilation](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 Erläutert die Kompilierung bestimmter Codeabschnitte.  
  
 [Erstellen und Bereinigen von Projekten und Projektmappen in Visual Studio](/visual-studio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio)  
 Beschreibt, wie Sie die Elemente verwalten, die in verschiedenen Builds zum Einsatz kommen sollen, Projekteigenschaften auswählen und sicherstellen, dass die Projekte in der richtigen Reihenfolge erstellt werden.