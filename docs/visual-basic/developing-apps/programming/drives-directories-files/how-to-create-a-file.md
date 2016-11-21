---
title: "How to: Create a File in Visual Basic | Microsoft Docs"
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
  - "text files, creating"
  - "files, creating"
ms.assetid: 0253bb6d-5519-4a50-b882-b93ef5cca0d9
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create a File in Visual Basic
In diesem Beispiel wird unter Verwendung der <xref:System.IO.File.Create%2A>\-Methode in der <xref:System.IO.File>\-Klasse eine Textdatei im angegebenen Pfad erstellt.  
  
## Beispiel  
 [!CODE [VbFileIOMisc#1](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOMisc#1)]  
  
## Kompilieren des Codes  
 Verwenden Sie zum Schreiben in die Datei die `file`\-Variable.  
  
## Robuste Programmierung  
 Wenn die Datei bereits vorhanden ist, wird sie ersetzt.  
  
 Unter den folgenden Bedingungen kann eine Ausnahme ausgelöst werden:  
  
-   Der Pfadname ist falsch formatiert.  Er enthält beispielsweise unzulässige Zeichen oder besteht nur aus Leerzeichen \(<xref:System.ArgumentException>\).  
  
-   Der Pfad ist schreibgeschützt \(<xref:System.IO.IOException>\).  
  
-   Der Pfadname ist `Nothing` \(<xref:System.ArgumentNullException>\).  
  
-   Der Pfadname ist zu lang \(<xref:System.IO.PathTooLongException>\).  
  
-   Der Pfad ist ungültig \(<xref:System.IO.DirectoryNotFoundException>\).  
  
-   Der Pfad besteht nur aus einem Doppelpunkt ":" \(<xref:System.NotSupportedException>\).  
  
## .NET Framework-Sicherheit  
 In teilweise vertrauenswürdigen Umgebungen kann eine <xref:System.Security.SecurityException> ausgelöst werden.  
  
 Für den Aufruf der <xref:System.IO.File.Create%2A>\-Methode benötigen Sie <xref:System.Security.Permissions.FileIOPermission>.  
  
 Wenn der Benutzer nicht über die Berechtigung zum Erstellen der Datei verfügt, wird eine <xref:System.UnauthorizedAccessException> ausgelöst.  
  
## Siehe auch  
 <xref:System.IO>   
 <xref:System.IO.File.Create%2A>   
 [Using Libraries from Partially Trusted Code](../Topic/Using%20Libraries%20from%20Partially%20Trusted%20Code.md)   
 [Code Access Security Basics](../Topic/Code%20Access%20Security%20Basics.md)