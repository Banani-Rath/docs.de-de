---
title: "&#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies/multiline lambdas | Microsoft Docs"
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
  - "bc32025"
  - "vbc32025"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC32025"
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies/multiline lambdas
Der `#Region`\-Block muss auf Klassen\-, Modul\- oder Namespaceebene deklariert werden.  Eine reduzierbare Region kann eine oder mehrere Prozeduren umfassen, kann aber nicht in einer Prozedur beginnen oder enden.  
  
 **Fehler\-ID:** BC32025  
  
### So beheben Sie diesen Fehler  
  
1.  Stellen Sie sicher, dass die vorangehende Prozedur ordnungsgemäß durch eine `End Function`\-Anweisung oder eine `End Sub`\-Anweisung beendet wird.  
  
2.  Stellen Sie sicher, dass die `#Region`\-Direktive und die `#End Region`\-Direktive im gleichen Codeblock enthalten sind.  
  
## Siehe auch  
 [\#Region Directive](../../../visual-basic/language-reference/directives/region-directive.md)