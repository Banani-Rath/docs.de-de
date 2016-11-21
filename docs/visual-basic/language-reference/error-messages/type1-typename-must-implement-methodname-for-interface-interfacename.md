---
title: "&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39; | Microsoft Docs"
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
  - "vbc30149"
  - "bc30149"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30149"
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;
Eine Klasse oder Struktur soll eine Schnittstelle implementieren. Dabei wird jedoch eine von der Schnittstelle definierte Prozedur nicht implementiert.  Jeder Member der Schnittstelle muss implementiert werden.  
  
 **Fehler\-ID:** BC30149  
  
### So beheben Sie diesen Fehler  
  
1.  Deklarieren Sie eine Prozedur mit demselben Namen und derselben Signatur wie in der Schnittstelle definiert.  Vergewissern Sie sich, dass mindestens die `End Function`\- oder `End Sub`\-Anweisung enthalten ist.  
  
2.  Fügen Sie am Ende der `Function`\- oder `Sub`\-Anweisung eine `Implements`\-Klausel an.  Beispiele:  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## Siehe auch  
 [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md)   
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)