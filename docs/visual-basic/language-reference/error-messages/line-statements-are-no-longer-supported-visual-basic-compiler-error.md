---
title: "&#39;Line&#39; statements are no longer supported (Visual Basic Compiler Error) | Microsoft Docs"
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
  - "bc30830"
  - "vbc30830"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30830"
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Line&#39; statements are no longer supported (Visual Basic Compiler Error)
Line\-Anweisungen werden nicht mehr unterstützt.  Dateiein\- und \-ausgaben sind als `Microsoft.VisualBasic.FileSystem.LineInput` verfügbar, und Grafikfunktionalität ist als `System.Drawing.Graphics.DrawLine` verfügbar.  
  
 **Fehler\-ID:** BC30830  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie zum Ausführen eines Dateizugriffs `Microsoft.VisualBasic.FileSystem.LineInput`.  
  
2.  Zur Ausführung von Grafikfunktionen verwenden Sie `System.Drawing.Graphics.Drawline`.  
  
## Siehe auch  
 <xref:System.IO>   
 <xref:System.Drawing>   
 [File Access with Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)