---
title: "How to: Create a String from An Array of Char Values (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
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
  - "examples [Visual Basic], arrays"
  - "examples [Visual Basic], Char data type"
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create a String from An Array of Char Values (Visual Basic)
Dieses Beispiel erstellt die Zeichenfolge "abcd" anhand von einzelnen Zeichen.  
  
## Beispiel  
 [!CODE [VbVbalrStrings#61](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#61)]  
  
## Kompilieren des Codes  
 Für diese Methode gelten keine besonderen Voraussetzungen.  
  
 Mit der Syntax `"a"c`, bei der ein einzelnes `c` auf ein Zeichen in Anführungszeichen folgt, wird ein Zeichenliteral erstellt.  
  
## Robuste Programmierung  
 Wenn die Zeichenfolge NULL\-Zeichen \(entspricht `Chr(0)`\) enthält, kann es bei der Verwendung der Zeichenfolge zu unerwarteten Ergebnissen kommen.  Das NULL\-Zeichen wird zwar der Zeichenfolge hinzugefügt; in bestimmten Situationen werden allerdings die darauf folgenden Zeichen nicht angezeigt.  
  
## Siehe auch  
 <xref:System.String>   
 [Char Data Type](../../../../visual-basic/language-reference/data-types/char-data-type.md)   
 [Datentypen](../../../../visual-basic/programming-guide/language-features/data-types/index.md)