---
title: "^= Operator (Visual Basic) | Microsoft Docs"
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
  - "vb.^="
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "assignment statements, compound"
  - "statements [Visual Basic], compound assignment"
  - "^= operator [Visual Basic]"
  - "compound assignment statements"
ms.assetid: 397da132-2d96-4a85-a7bc-f7c730a608c9
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# ^= Operator (Visual Basic)
Erhebt den Wert einer Variablen oder Eigenschaft zur Potenz eines Ausdrucks und weist das Ergebnis der Variablen oder Eigenschaft zu.  
  
## Syntax  
  
```  
  
variableorproperty ^= expression  
```  
  
## Teile  
 `variableorproperty`  
 Erforderlich.  Beliebige numerische Variable oder Eigenschaft.  
  
 `expression`  
 Erforderlich.  Ein beliebiger numerischer Ausdruck.  
  
## Hinweise  
 Das Element auf der linken Seite des Operators `^=` kann eine einfache Skalarvariable, eine Eigenschaft oder ein Element eines Arrays sein.  Die Variable oder die Eigenschaft kann nicht [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)sein.  
  
 Der Operator `^=` wird anfänglich den Wert der Variablen oder Eigenschaft auf der linken Seite des Operators\) mit dem Wert des Ausdrucks durch \(auf der rechten Seite des Operators\).  Der Operator weist dann das Ergebnis dieses Vorgangs wieder in der Variablen oder Eigenschaft zu.  
  
 Visual Basic führt eine Potenzierung immer mit dem [Double Data Type](../../../visual-basic/language-reference/data-types/double-data-type.md) aus.  Operanden eines anderen Typs werden in `Double` konvertiert. Als Ergebnis wird immer ein Wert vom `Double`\-Typ ermittelt.  
  
 Der Wert von `expression` kann ein Bruch, negativ oder beides sein.  
  
## Überladen  
 Der [^ Operator](../../../visual-basic/language-reference/operators/exponentiation-operator.md) kann *überladen* werden. Das bedeutet, dass eine Klasse oder Struktur sein Verhalten neu definiert, wenn ein Operand den Typ dieser Klasse oder Struktur aufweist.  Das Überladen des Operators `^` hat Auswirkungen auf das Verhalten des Operators `^=`.  Wenn im Code `^=` auf eine Klasse oder Struktur angewendet wird, die `^` überlädt, sollten Sie auf jeden Fall sein neu definiertes Verhalten verstehen.  Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Beispiel  
 Im folgenden Beispiel wird der Operator `^=` verwendet, um den Wert einer `Integer`\-Variablen mit einer zweiten Variablen zu potenzieren und das Ergebnis der ersten Variablen zuzuweisen.  
  
 [!CODE [VbVbalrOperators#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#21)]  
  
## Siehe auch  
 [^ Operator](../../../visual-basic/language-reference/operators/exponentiation-operator.md)   
 [Assignment Operators](../../../visual-basic/language-reference/operators/assignment-operators.md)   
 [Arithmetic Operators](../../../visual-basic/language-reference/operators/arithmetic-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [Statements](../../../visual-basic/programming-guide/language-features/statements.md)