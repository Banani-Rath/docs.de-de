---
title: "No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39; | Microsoft Docs"
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
  - "bc30737"
  - "vbc30737"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30737"
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39;
In Befehlszeilenanwendungen muss eine `Sub Main`\-Prozedur definiert sein.  In Klassendeklarationen muss `Main` als `Public Shared` deklariert werden, in einer Moduldeklaration als `Public`.  
  
 Weitere Informationen zu `Main` finden Sie unter [NIB: Visual Basic Version of Hello, World](http://msdn.microsoft.com/de-de/9d030b60-e148-4366-a462-69532f02294c).  
  
 **Fehler\-ID:** BC30737  
  
### So beheben Sie diesen Fehler  
  
-   Definieren Sie eine `Public Sub Main`\-Prozedur für das Projekt.  Deklarieren Sie sie nur dann als `Shared`, wenn sie in einer Klasse definiert ist.  
  
## Siehe auch  
 [NIB: Visual Basic Version of Hello, World](http://msdn.microsoft.com/de-de/9d030b60-e148-4366-a462-69532f02294c)   
 [Structure of a Visual Basic Program](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)   
 [Procedures](../../../visual-basic/programming-guide/language-features/procedures/index.md)