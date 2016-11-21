---
title: "ByVal (Visual Basic) | Microsoft Docs"
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
  - "vb.ByVal"
  - "ByVal"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "ByVal keyword, contexts"
  - "ByVal keyword"
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# ByVal (Visual Basic)
Kennzeichnet ein Argument, das so übergeben wird, dass der Wert einer Variablen, die dem Argument im Aufrufcode zugrunde liegt, von der aufgerufenen Prozedur oder Eigenschaft nicht geändert werden kann.  
  
## Hinweise  
 Der `ByVal`\-Modifizierer kann in folgenden Kontexten verwendet werden:  
  
 [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Operator Statement](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub Statement](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## Beispiel  
 Im folgenden Beispiel wird die Verwendung des Übergabemechanismus für den `ByVal`\-Parameter mit einem Referenztypargument veranschaulicht.  Im Beispiel ist das `c1`\-Argument eine Instanz der `Class1`\-Klasse.  `ByVal` verhindert, dass der zugrunde liegende Wert des `c1`\-Verweisarguments vom Code in den Prozeduren geändert wird, die Felder und Eigenschaften von `c1`, auf die zugegriffen werden kann, sind jedoch nicht geschützt.  
  
 [!CODE [VbVbalrKeywords#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#10)]  
  
## Siehe auch  
 [Stichwörter](../../../visual-basic/language-reference/keywords/index.md)   
 [Passing Arguments by Value and by Reference](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)