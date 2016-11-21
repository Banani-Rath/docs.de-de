---
title: "Object or class does not support the set of events | Microsoft Docs"
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
  - "vbrID459"
dev_langs: 
  - "VB"
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Object or class does not support the set of events
Sie haben versucht, eine `WithEvents`\-Variable mit einer Komponente zu verwenden, die nicht als Ereignisquelle für den angegebenen Satz von Ereignissen fungieren kann.  Sie haben z. B. versucht, die Ereignisse eines Objekts aufzufangen und anschließend ein anderes Objekt zu erstellen, das das erste Objekt `Implements`.  Es ist nicht immer möglich, die Ereignisse aus dem implementierten Objekt aufzufangen.  Mit `Implements` wird nur eine Schnittstelle für Methoden und Eigenschaften implementiert.  `WithEvents` wird für private`UserControls` nicht unterstützt, da die Typinformationen zum Auslösen von `ObjectEvent` zur Laufzeit nicht verfügbar sind.  
  
### So beheben Sie diesen Fehler  
  
1.  Sie können keine Ereignisse für eine Komponente auffangen, die keine Ereignisse generiert.  
  
## Siehe auch  
 [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)   
 [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md)