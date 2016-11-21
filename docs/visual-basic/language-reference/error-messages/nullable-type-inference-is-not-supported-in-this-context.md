---
title: "Nullable type inference is not supported in this context | Microsoft Docs"
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
  - "vbc36629"
  - "bc36629"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC36629"
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Nullable type inference is not supported in this context
Werttypen und Strukturen können so deklariert werden, dass sie NULL\-Werte zulassen.  
  
```vb#  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 Die auf NULL festlegbare Deklaration kann jedoch nicht in Verbindung mit dem Typrückschluss verwendet werden.  Dieser Fehler wird durch die folgenden Beispiele verursacht.  
  
```vb#  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **Fehler\-ID:** BC36629  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie eine `As`\-Klausel, um die Variable so zu deklarieren, dass sie NULL\-Werte zulässt.  
  
## Siehe auch  
 [Nullable Value Types](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)   
 [Local Type Inference](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)