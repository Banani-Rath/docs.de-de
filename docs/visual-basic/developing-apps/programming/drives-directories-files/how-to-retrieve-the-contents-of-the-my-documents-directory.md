---
title: "How to: Retrieve the Contents of the My Documents Directory in Visual Basic | Microsoft Docs"
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
  - "My Documents directory"
ms.assetid: 26560d01-7dda-4457-8e95-21db23d71aea
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Retrieve the Contents of the My Documents Directory in Visual Basic
Mit dem <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>\-Objekt können Inhalte aus vielen der **Alle Benutzer**\-Verzeichnisse gelesen werden, z. B. aus **Eigene Dateien** oder **Desktop**.  
  
### So lesen Sie Inhalte aus dem Ordner Eigene Dateien  
  
-   Mit der `ReadAllText`\-Methode können Sie den Text aus jeder Datei in einem bestimmten Verzeichnis lesen.  Im folgenden Code wird ein Verzeichnis und eine Datei angegeben und deren Inhalt mithilfe von `ReadAllText` in eine Zeichenfolge mit dem Namen `patients` eingelesen.  
  
     [!CODE [VbVbcnMyFileSystem#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMyFileSystem#15)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.ReadAllText%2A>