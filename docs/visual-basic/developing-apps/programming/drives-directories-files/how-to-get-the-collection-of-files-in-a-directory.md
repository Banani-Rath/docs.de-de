---
title: "How to: Get the Collection of Files in a Directory in Visual Basic | Microsoft Docs"
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
  - "folders, working with"
  - "files, accessing"
ms.assetid: 6c8ba7e8-dd37-4853-92bf-762b67c98160
caps.latest.revision: 23
caps.handback.revision: 23
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Get the Collection of Files in a Directory in Visual Basic
Die Überladungen der <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A?displayProperty=fullName>\-Methode geben eine schreibgeschützte Sammlung an Zeichenfolgen zurück, die die Namen der Dateien innerhalb eines Verzeichnisses darstellen:  
  
-   Verwenden Sie die <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%28System.String%29>\-Überladung für eine einfache Dateisuche in einem angegebenen Verzeichnis, ohne Unterverzeichnisse zu durchsuchen.  
  
-   Verwenden Sie die [GetFiles\(String, SearchOption, String\[\]\)](assetId:///M:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles(System.String,Microsoft.VisualBasic.FileIO.SearchOption,System.String[])?qualifyHint=False&autoUpgrade=False)\-Überladung, um zusätzliche Optionen für Ihre Suche anzugeben.  Sie können die `wildCards`\-Parameter verwenden, um ein Suchmuster anzugeben.  Legen Sie zum Einschließen der Unterverzeichnisse in die Suche den Parameter `searchType` auf <xref:Microsoft.VisualBasic.FileIO.SearchOption?displayProperty=fullName> fest.  
  
 Es wird eine leere Sammlung zurückgegeben, wenn keine Dateien dem angegebenen Muster entsprechen.  
  
### So listen Sie Dateien in einem Verzeichnis auf  
  
-   Verwenden Sie eine der <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A?displayProperty=fullName>\-Methodenüberladungen, geben Sie den Namen und Pfad des zu durchsuchenden Verzeichnisses im Parameter `directory` an.  Im folgenden Beispiel werden alle Dateien im Verzeichnis zurückgegeben und  `ListBox1` hinzugefügt.  
  
     [!CODE [VbVbcnMyFileSystem#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#32)]  
  
## Robuste Programmierung  
 Die folgenden Bedingungen können einen Ausnahmefehler verursachen:  
  
-   Der Pfad ist aus einem der folgenden Gründe ungültig: Es handelt sich um eine Zeichenfolge der Länge 0, der Pfad enthält nur Leerzeichen, er enthält ungültige Zeichen, oder es handelt sich um einen Gerätepfad \(beginnt mit \\\\.  \\\) \(<xref:System.ArgumentException>\).  
  
-   Der Pfad ist ungültig, da er `Nothing` ist \(<xref:System.ArgumentNullException>\).  
  
-   `directory` existiert nicht \(<xref:System.IO.DirectoryNotFoundException>\).  
  
-   `directory` verweist auf eine bestehende Datei \(<xref:System.IO.IOException>\).  
  
-   Der Pfad überschreitet die im System definierte maximale Länge \(<xref:System.IO.PathTooLongException>\).  
  
-   Der Pfad eines Datei\- oder Verzeichnisnamens enthält einen Doppelpunkt \(:\) oder hat ein ungültiges Format \(<xref:System.NotSupportedException>\).  
  
-   Dem Benutzer fehlen die erforderlichen Berechtigungen zum Anzeigen des Pfades \(<xref:System.Security.SecurityException>\).  
  
-   Der Benutzer verfügt nicht über die erforderlichen Berechtigungen \(<xref:System.UnauthorizedAccessException>\).  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.GetFiles%2A>   
 [How to: Find Files with a Specific Pattern](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-files-with-a-specific-pattern.md)   
 [How to: Find Subdirectories with a Specific Pattern](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-subdirectories-with-a-specific-pattern.md)