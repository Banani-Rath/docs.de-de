---
title: "Argument not optional (Visual Basic) | Microsoft Docs"
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
  - "vbrID449"
dev_langs: 
  - "VB"
ms.assetid: 76e7bcf3-24ed-4cd5-945b-b98f1c76944b
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Argument not optional (Visual Basic)
Argumentanzahl und \-typen müssen mit der erwarteten Anzahl bzw. den erwarteten Typen übereinstimmen.  Es gibt zwei Möglichkeiten: Die Anzahl der Argumente ist falsch, oder es wurde ein nicht optionales Argument ausgelassen.  Ein Argument kann nur dann in einem Aufruf einer benutzerdefinierten Prozedur ausgelassen werden, wenn es in der Prozedurdefinition als `Optional` deklariert wurde.  
  
### So beheben Sie diesen Fehler  
  
1.  Geben Sie alle notwendigen Argumente an.  
  
2.  Stellen Sie sicher, dass nur optionale Argumente ausgelassen wurden.  Andernfalls geben Sie das Argument entweder im Aufruf an oder deklarieren den Parameter in der Definition als `Optional`.  
  
## Siehe auch  
 [Error Types](../../../visual-basic/programming-guide/language-features/error-types.md)