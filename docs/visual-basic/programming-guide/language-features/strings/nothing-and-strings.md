---
title: "Nothing and Strings in Visual Basic | Microsoft Docs"
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
  - "strings [Visual Basic], Nothing"
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Nothing and Strings in Visual Basic
Die [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Laufzeit und [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] werten `Nothing` für Zeichenfolgen unterschiedlich aus.  
  
## Visual Basic\-Laufzeit und .NET Framework  
 Betrachten Sie das folgende Beispiel:  
  
 [!CODE [VbVbalrStrings#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#47)]  
  
 Die [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Laufzeit wertet `Nothing` normalerweise als leere Zeichenfolge \(""\) aus.  [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] tut dies jedoch nicht und löst eine Ausnahme aus, sobald versucht wird, eine Zeichenfolgenoperation an `Nothing` auszuführen.  
  
## Siehe auch  
 [Introduction to Strings in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)