---
title: "\= Operator | Microsoft Docs"
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
  - "\="
  - "vb.\="
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "\= operator [Visual Basic]"
  - "assignment statements, compound"
  - "statements [Visual Basic], compound assignment"
  - "operator \= [Visual Basic]"
  - "compound assignment statements"
ms.assetid: 6f39915d-e398-4045-afcc-da6885e57b9c
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# \= Operator
Dividiert den Wert einer Variablen oder Eigenschaft durch den Wert eines Ausdrucks und weist die sich daraus ergebende ganze Zahl der Variablen oder Eigenschaft zu.  
  
## Syntax  
  
```  
  
variableorproperty \= expression  
```  
  
## Teile  
 `variableorproperty`  
 Erforderlich.  Beliebige numerische Variable oder Eigenschaft.  
  
 `expression`  
 Erforderlich.  Ein beliebiger numerischer Ausdruck.  
  
## Hinweise  
 Das Element auf der linken Seite des Operators `\=` kann eine einfache Skalarvariable, eine Eigenschaft oder ein Element eines Arrays sein.  Die Variable oder die Eigenschaft kann nicht [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)sein.  
  
 Der `\=` Operator teilt der Wert einer Variablen oder Eigenschaft auf der linken Seite durch den Wert für das Recht ganzzahlige und weist das Ergebnis der Variablen oder Eigenschaft auf der linken Seite an  
  
 Weitere Informationen über die Division ganzer Zahlen finden Sie unter [\\ Operator](../../../visual-basic/language-reference/operators/integer-division-operator.md).  
  
## Überladen  
 Der Operator `\` kann *überladen* werden. Das bedeutet, dass eine Klasse oder Struktur sein Verhalten neu definiert, wenn ein Operand den Typ dieser Klasse oder Struktur aufweist.  Das Überladen des Operators `\` hat Auswirkungen auf das Verhalten des Operators `\=`.  Wenn im Code `\=` auf eine Klasse oder Struktur angewendet wird, die `\` überlädt, sollten Sie auf jeden Fall sein neu definiertes Verhalten verstehen.  Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Beispiel  
 Im folgenden Beispiel wird der Operator `\=` verwendet, um eine `Integer`\-Variable durch eine andere zu dividieren und das ganzzahlige Ergebnis der ersten Variablen zuzuweisen.  
  
 [!CODE [VbVbalrOperators#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#19)]  
  
## Siehe auch  
 [\\ Operator](../../../visual-basic/language-reference/operators/integer-division-operator.md)   
 [\/\= Operator](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)   
 [Assignment Operators](../../../visual-basic/language-reference/operators/assignment-operators.md)   
 [Arithmetic Operators](../../../visual-basic/language-reference/operators/arithmetic-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [Statements](../../../visual-basic/programming-guide/language-features/statements.md)