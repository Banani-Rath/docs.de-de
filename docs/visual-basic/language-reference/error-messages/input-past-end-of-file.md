---
title: "Input past end of file | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbrID62"
dev_langs: 
  - "VB"
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Input past end of file
Entweder wird mit einer `Input`\-Anweisung aus einer Datei gelesen, die leer ist oder in der alle Daten verwendet werden, oder Sie haben die `EOF`\-Funktion mit einer Datei verwendet, die im binären Zugriffsmodus geöffnet ist.  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie die `EOF`\-Funktion unmittelbar vor der `Input`\-Anweisung, um das Dateiende festzustellen.  
  
2.  Wenn die Datei im binären Zugriffsmodus geöffnet wurde, verwenden Sie `Seek` und `Loc`.  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileSystem.Input%2A>   
 <xref:Microsoft.VisualBasic.FileSystem.EOF%2A>   
 <xref:Microsoft.VisualBasic.FileSystem.Seek%2A>   
 <xref:Microsoft.VisualBasic.FileSystem.Loc%2A>