---
title: "Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement | Microsoft Docs"
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
  - "vbc30157"
  - "bc30157"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30157"
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Leading &#39;.&#39; or &#39;!&#39; can only appear inside a &#39;With&#39; statement
Ein Punkt \(.\) oder ein Ausrufezeichen \(\!\), der bzw. das sich nicht innerhalb eines `With`\-Blocks befindet, tritt ohne Ausdruck auf der linken Seite auf.  Memberzugriff \(`.`\) und Dictionary\-Memberzugriff \(`!`\) erfordern einen Ausdruck, der das Element angibt, das den Member enthält.  Dieser muss direkt links neben dem Accessor oder als Ziel eines `With`\-Blocks stehen, der den Memberzugriff enthält.  
  
 **Fehler\-ID:** BC30157  
  
### So beheben Sie diesen Fehler  
  
1.  Vergewissern Sie sich, dass der `With`\-Block richtig formatiert ist.  
  
2.  Wenn kein `With`\-Block vorhanden ist, fügen Sie links neben dem Accessor, der ein definiertes Element mit dem Member ergibt, einen Ausdruck hinzu.  
  
## Siehe auch  
 [Special Characters in Code](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)   
 [With...End With Statement](../../../visual-basic/language-reference/statements/with-end-with-statement.md)