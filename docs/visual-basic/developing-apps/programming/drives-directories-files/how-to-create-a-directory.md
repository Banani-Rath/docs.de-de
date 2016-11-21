---
title: "How to: Create a Directory in Visual Basic | Microsoft Docs"
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
  - "directories [Visual Basic], creating"
  - "folders [Visual Basic], creating"
ms.assetid: 0351a2ca-24d8-43b5-bb39-9b99e6401cff
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create a Directory in Visual Basic
Verwenden Sie die `CreateDirectory`\-Methode des `My.Computer.FileSystem`\-Objekts zum Erstellen von Verzeichnissen.  
  
 Wenn das Verzeichnis bereits vorhanden ist, wird keine Ausnahme ausgelöst.  
  
### So erstellen Sie ein Verzeichnis  
  
-   Verwenden Sie die `CreateDirectory`\-Methode, und geben Sie den vollständigen Pfad für das zu erstellende Verzeichnis an.  In diesem Beispiel wird das Verzeichnis `NewDirectory` unter `C:\Documents and Settings\All Users\Documents` erstellt.  
  
     [!CODE [VbVbcnMyFileSystem#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#2)]  
  
## Robuste Programmierung  
 Unter den folgenden Bedingungen kann eine Ausnahme ausgelöst werden:  
  
-   Der Verzeichnisname ist falsch formatiert.  Er enthält beispielsweise unzulässige Zeichen oder besteht nur aus Leerzeichen \(<xref:System.ArgumentException>\).  
  
-   Das übergeordnete Verzeichnis des zu erstellenden Verzeichnisses ist schreibgeschützt \(<xref:System.IO.IOException>\).  
  
-   Der Verzeichnisname ist `Nothing` \(<xref:System.ArgumentNullException>\).  
  
-   Der Verzeichnisname ist zu lang \(<xref:System.IO.PathTooLongException>\).  
  
-   Der Verzeichnisname besteht nur aus einem Doppelpunkt ":" \(<xref:System.NotSupportedException>\).  
  
-   Der Benutzer ist nicht zum Erstellen des Verzeichnisses berechtigt \(<xref:System.UnauthorizedAccessException>\).  
  
-   Dem Benutzer fehlen Berechtigungen in einer teilweise vertrauenswürdigen Situation \(<xref:System.Security.SecurityException>\).  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.CreateDirectory%2A>   
 [Creating, Deleting, and Moving Files and Directories](../../../../visual-basic/developing-apps/programming/drives-directories-files/creating-deleting-and-moving-files-and-directories.md)