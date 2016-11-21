---
title: "How to: Pass Procedures to Another Procedure in Visual Basic | Microsoft Docs"
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
  - "AddressOf operator"
  - "delegates [Visual Basic], passing procedures"
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Pass Procedures to Another Procedure in Visual Basic
In diesem Beispiel wird veranschaulicht, wie mithilfe von Delegaten eine Prozedur an eine andere Prozedur übergeben wird.  
  
 Ein Delegat ist ein Typ, den Sie wie jeden anderen Typ in [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] verwenden können.  Wenn der Operator `AddressOf` auf einen Prozedurnamen angewendet wird, gibt er ein Delegatobjekt zurück.  
  
 Im vorliegenden Beispiel liegt eine Prozedur mit einem Delegatparameter vor. Dieser kann eine Referenz an eine andere Prozedur enthalten, die mit dem Operator `AddressOf` abgerufen wird.  
  
### Erstellen des Delegaten und entsprechender Prozeduren  
  
1.  Erstellen Sie einen Delegaten mit dem Namen `MathOperator`.  
  
     [!CODE [VbVbalrDelegates#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#1)]  
  
2.  Erstellen Sie eine Prozedur mit dem Namen `AddNumbers` mit Parametern und einem Rückgabewert. Diese müssen mit denjenigen von `MathOperator` übereinstimmen, da andernfalls unterschiedliche Signaturen vorliegen.  
  
     [!CODE [VbVbalrDelegates#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#2)]  
  
3.  Erstellen Sie eine Prozedur mit dem Namen `SubtractNumbers` mit einer Signatur, die der von `MathOperator` entspricht.  
  
     [!CODE [VbVbalrDelegates#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#3)]  
  
4.  Erstellen Sie eine Prozedur mit dem Namen `DelegateTest`, der als Parameter ein Delegat übergeben wird.  
  
     Dieser Prozedur kann ein Verweis auf `AddNumbers` oder `SubtractNumbers` übergeben werden, weil deren Signaturen der Signatur von `MathOperator` entsprechen.  
  
     [!CODE [VbVbalrDelegates#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#4)]  
  
5.  Erstellen Sie eine Prozedur mit dem Namen `Test`, die `DelegateTest` einmal mit dem Delegaten für `AddNumbers` als Parameter und ein zweites Mal mit dem Delegaten für `SubtractNumbers` als Parameter aufruft.  
  
     [!CODE [VbVbalrDelegates#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDelegates#5)]  
  
     Beim Aufruf von `Test` wird zuerst das Ergebnis von `AddNumbers` angezeigt. Dabei wird die Summe aus `5` und `3` gebildet, also 8.  Anschließend wird das Ergebnis des Vorgangs `SubtractNumbers` angezeigt. Dabei wird die Differenz zwischen `9` und `3` ermittelt, also 6.  
  
## Siehe auch  
 [Delegates](../../../../visual-basic/programming-guide/language-features/delegates/delegates.md)   
 [AddressOf Operator](../../../../visual-basic/language-reference/operators/addressof-operator.md)   
 [Delegate Statement](../../../../visual-basic/language-reference/statements/delegate-statement.md)   
 [How to: Invoke a Delegate Method](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)