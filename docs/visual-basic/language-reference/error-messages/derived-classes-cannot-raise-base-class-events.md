---
title: "Derived classes cannot raise base class events | Microsoft Docs"
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
  - "vbc30029"
  - "bc30029"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30029"
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Derived classes cannot raise base class events
Ein Ereignis kann nur vom Deklarationsabschnitt ausgelöst werden, in dem es deklariert wurde.  Daher kann eine Klasse keine Ereignisse aus einer anderen Klasse auslösen, auch nicht aus einer Klasse, aus der sie abgeleitet wurde.  
  
 **Fehler\-ID:** BC30029  
  
### So beheben Sie diesen Fehler  
  
-   Verschieben Sie die `Event`\- oder `RaiseEvent`\-Anweisung, sodass sie in derselben Klasse stehen.  
  
## Siehe auch  
 [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md)   
 [RaiseEvent Statement](../../../visual-basic/language-reference/statements/raiseevent-statement.md)