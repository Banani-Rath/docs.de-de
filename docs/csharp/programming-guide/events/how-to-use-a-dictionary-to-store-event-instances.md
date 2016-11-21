---
title: "Gewusst wie: Verwenden eines W&#246;rterbuchs zum Speichern von Ereignisinstanzen (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Ereignisse [C#], Speichern von Instanzen in einem Wörterbuch"
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden eines W&#246;rterbuchs zum Speichern von Ereignisinstanzen (C#-Programmierhandbuch)
Unter anderem können `accessor-declarations` auch verwendet werden, um viele Ereignisse verfügbar zu machen, ohne dass für jedes Ereignis ein Feld reserviert werden muss. Stattdessen werden die Ereignisinstanzen in einem Wörterbuch gespeichert.  Dies ist nur dann nützlich, wenn viele Ereignisse vorhanden sind, Sie jedoch davon ausgehen, dass die meisten Ereignisse nicht implementiert werden.  
  
## Beispiel  
 [!CODE [csProgGuideEvents#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEvents#9)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Ereignisse](../../../csharp/programming-guide/events/index.md)   
 [Delegaten](../../../csharp/programming-guide/delegates/index.md)