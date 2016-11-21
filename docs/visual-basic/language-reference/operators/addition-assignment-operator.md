---
title: "+= Operator (Visual Basic) | Microsoft Docs"
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
  - "vb.+="
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "+= operator [Visual Basic]"
  - "assignment statements, compound"
  - "statements [Visual Basic], compound assignment"
  - "+= operator [Visual Basic], appending strings"
  - "compound assignment statements"
ms.assetid: d3e959f4-85d4-4e47-87c4-77b62335a5b3
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# += Operator (Visual Basic)
Addiert den Wert eines numerischen Ausdrucks zum Wert einer numerischen Variablen oder Eigenschaft und weist der Variablen bzw. der Eigenschaft das Ergebnis zu.  Kann auch verwendet werden, um einen `String`\-Ausdruck mit einer `String`\-Variablen oder String\-Eigenschaft zu verketten und der Variablen bzw. Eigenschaft das Ergebnis zuzuweisen.  
  
## Syntax  
  
```  
  
variableorproperty += expression  
```  
  
## Teile  
 `variableorproperty`  
 Erforderlich.  Beliebige numerische Variable\/Eigenschaft oder beliebige `String`\-Variable\/\-Eigenschaft.  
  
 `expression`  
 Erforderlich.  Beliebiger numerischer oder `String`\-Ausdruck.  
  
## Hinweise  
 Das Element auf der linken Seite des Operators `+=` kann eine einfache Skalarvariable, eine Eigenschaft oder ein Element eines Arrays sein.  Die Variable oder die Eigenschaft kann nicht [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md)sein.  
  
 Der `+=`\-Operator fügt den Wert für das Recht der Variablen oder Eigenschaft auf der linken Seite hinzu und weist das Ergebnis der Variablen oder Eigenschaft auf der linken Seite.  Der `+=`\-Operator kann auch verwendet werden, um den `String` Ausdruck für das Recht zur `String`\-Variablen oder Eigenschaft auf der linken Seite zu verketten und weist das Ergebnis der Variablen oder Eigenschaft auf der linken Seite.  
  
> [!NOTE]
>  Wenn Sie den Operator `+=` verwenden, können Sie nicht immer bestimmen, ob eine Addition oder eine Zeichenverkettung erfolgt.  Verwenden Sie für die Verkettung den Operator `&=`, um Mehrdeutigkeiten zu vermeiden und sich selbst dokumentierenden Code zu erhalten.  
  
 Dieser Zuweisungsoperator führt implizit erweiternde Konvertierungen durch, jedoch keine einschränkende Konvertierungen, wenn die Kompilierungsumgebung eine strikte Semantik zwingend vorgibt.  Weitere Informationen zu diesen Konvertierungen finden Sie unter [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).  Weitere Informationen zur strikten und zur freien Semantik finden Sie unter [Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md).  
  
 Wenn eine freie Semantik erlaubt ist, führt der Operator `+=` implizit eine Reihe von Zeichenfolgenkonvertierungen und numerischen Konvertierungen durch, die mit denen des Operators `+` identisch sind.  Ausführliche Informationen zu diesen Konvertierungen finden Sie unter [\+ Operator](../../../visual-basic/language-reference/operators/addition-operator.md).  
  
## Überladen  
 Der Operator `+` kann *überladen* werden. Das bedeutet, dass eine Klasse oder Struktur sein Verhalten neu definiert, wenn ein Operand den Typ dieser Klasse oder Struktur aufweist.  Das Überladen des Operators `+` hat Auswirkungen auf das Verhalten des Operators `+=`.  Wenn im Code `+=` für eine Klasse oder Struktur verwendet wird, die `+` überlädt, müssen Sie das neu definierte Verhalten verstehen.  Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Beispiel  
 Im folgenden Beispielen wird der Operator `+=` verwendet, um die Werte zweier Variablen zu kombinieren.  Der erste Teil verwendet `+=` mit numerischen Variablen, um einen Wert zu einem anderen hinzuzuaddieren.  Der zweite Teil verwendet `+=` mit `String`\-Variablen, um einen Wert mit einem anderen Wert zu verketten.  In beiden Fällen wird das Ergebnis der ersten Variablen zugewiesen.  
  
 [!CODE [VbVbalrOperators#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#7)]  
  
 [!CODE [VbVbalrOperators#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#8)]  
  
 Der Wert von `num1` ist jetzt 13, und der Wert von `str1` ist jetzt "103".  
  
## Siehe auch  
 [\+ Operator](../../../visual-basic/language-reference/operators/addition-operator.md)   
 [Assignment Operators](../../../visual-basic/language-reference/operators/assignment-operators.md)   
 [Arithmetic Operators](../../../visual-basic/language-reference/operators/arithmetic-operators.md)   
 [Concatenation Operators](../../../visual-basic/language-reference/operators/concatenation-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [Statements](../../../visual-basic/programming-guide/language-features/statements.md)