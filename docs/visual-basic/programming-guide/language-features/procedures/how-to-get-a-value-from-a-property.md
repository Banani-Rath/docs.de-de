---
title: "How to: Get a Value from a Property (Visual Basic) | Microsoft Docs"
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
  - "property values"
  - "Visual Basic code, procedures"
  - "values, properties"
  - "Visual Basic code, properties"
  - "properties [Visual Basic], values"
ms.assetid: 3954423e-6ab7-4a4c-b55c-a8d27be47891
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Get a Value from a Property (Visual Basic)
Sie rufen den Wert einer Eigenschaft ab, indem Sie den Eigenschaftennamen in einen Ausdruck einfügen.  
  
 Die `Get`\-Prozedur der Eigenschaft ruft den Wert ab, aber Sie rufen ihn nicht explizit über den Namen auf.  Sie verwenden die Eigenschaft wie eine Variable.  [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] ruft die Prozeduren der Eigenschaft auf.  
  
### So rufen Sie einen Wert aus einer Eigenschaft ab  
  
1.  Verwenden Sie den Eigenschaftennamen in einem Ausdruck auf die gleiche Weise, wie Sie einen Variablennamen verwenden würden.  Sie können eine Eigenschaft überall dort verwenden, wo Sie eine Variable oder eine Konstante verwenden können.  
  
     \- oder \-  
  
     Fügen Sie den Eigenschaftennamen hinter dem Gleichheitszeichen \(`=`\) in einer Zuweisungsanweisung ein.  
  
     Im folgenden Beispiel wird der Wert der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] `Now`\-Eigenschaft gelesen und die `Get`\-Prozedur implizit aufgerufen.  
  
     [!CODE [VbVbalrDateProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDateProperties#4)]  
  
2.  Wenn die Eigenschaft Argumente annimmt, fügen Sie nach dem Eigenschaftennamen runde Klammern ein, die die Argumentliste einschließen.  Wenn keine Argumente vorliegen, können Sie die Klammern auch weglassen.  
  
3.  Platzieren Sie die Argumente in der Argumentliste innerhalb der Klammern, und trennen Sie die Argumente durch Kommas.  Geben Sie die Argumente unbedingt in genau der Reihenfolge an, in der die Eigenschaft die entsprechenden Parameter definiert.  
  
 Der Wert der Eigenschaft hat im Ausdruck die gleiche Funktion wie eine Variable oder Konstante. Andernfalls wird er in der Variablen oder Eigenschaft auf der linken Seite der Zuweisungsanweisung gespeichert.  
  
## Siehe auch  
 [Procedures](../../../../visual-basic/programming-guide/language-features/procedures/index.md)   
 [Eigenschaftenprozeduren](../../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)   
 [Procedure Parameters and Arguments](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)   
 [Property Statement](../../../../visual-basic/language-reference/statements/property-statement.md)   
 [Differences Between Properties and Variables in Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/differences-between-properties-and-variables.md)   
 [How to: Create a Property](../../../../visual-basic/programming-guide/language-features/procedures/how-to-create-a-property.md)   
 [How to: Declare a Property with Mixed Access Levels](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)   
 [How to: Call a Property Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-call-a-property-procedure.md)   
 [How to: Declare and Call a Default Property in Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md)   
 [How to: Put a Value in a Property](../../../../visual-basic/programming-guide/language-features/procedures/how-to-put-a-value-in-a-property.md)