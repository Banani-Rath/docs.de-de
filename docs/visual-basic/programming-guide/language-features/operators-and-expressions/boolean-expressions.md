---
title: "Boolean Expressions (Visual Basic) | Microsoft Docs"
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
  - "short-circuiting"
  - "Boolean expressions"
  - "logical operators, Boolean expressions"
  - "expressions [Visual Basic], Boolean"
  - "expression evaluation, Boolean expressions"
  - "operators [Visual Basic], short-circuiting"
  - "Visual Basic code, operators"
  - "short-circuit evaluation"
  - "logical operators, short-circuiting"
  - "operators [Visual Basic], Boolean"
  - "Visual Basic code, expressions"
ms.assetid: d3d90406-55c8-4404-8143-50fd7f0d0d1a
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Boolean Expressions (Visual Basic)
Ein *boolescher Ausdruck* ist ein Ausdruck, der zu einem Wert mit dem [Boolean\-Datentyp](../../../../visual-basic/language-reference/data-types/boolean-data-type.md) ausgewertet wird: `True` oder `False`.  `Boolean`\-Ausdrücke können verschiedene Formen aufweisen.  Die einfachste Form ist der direkte Vergleich des Werts einer `Boolean`\-Variablen mit einem `Boolean`\-Literal, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrOperators#87](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#87)]  
  
## Zwei Bedeutungen des Operators '\='  
 Beachten Sie, dass die Zuweisungsanweisung `newCustomer = True` wie der Ausdruck im vorherigen Beispiel aussieht. Sie führt jedoch eine andere Funktion aus und wird auf eine andere Art verwendet.  Im vorherigen Beispiel stellt der Ausdruck `newCustomer = True` einen booleschen Wert dar, und das Zeichen `=` wird als Vergleichsoperator interpretiert.  In einer eigenständigen Anweisung wird das Zeichen `=` als Zuweisungsoperator interpretiert, und der Wert auf der rechten Seite wird der Variablen auf der linken Seite zugewiesen.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 [!CODE [VbVbalrOperators#88](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#88)]  
  
 Weitere Informationen finden Sie unter [Value Comparisons](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md) und unter [Statements](../../../../visual-basic/language-reference/statements/index.md).  
  
## Vergleichsoperatoren  
 Vergleichsoperatoren, z. B. `=`, `<`, `>`, `<>`, `<=` und `>=`, ergeben boolesche Ausdrücke, indem der Ausdruck auf der linken Seite des Operators mit dem Ausdruck auf der rechten Seite des Operators verglichen und das Ergebnis als `True` oder `False` ausgewertet wird.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 `42 < 81`  
  
 Da 42 kleiner als 81 ist, ergibt der boolesche Ausdruck im vorangehenden Beispiel `True`.  Weitere Informationen über diese Art von Ausdrücken finden Sie unter [Value Comparisons](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md).  
  
### Vergleichsoperatoren kombiniert mit logischen Operatoren  
 Vergleichsausdrücke können mithilfe von logischen Operatoren kombiniert werden, um komplexere boolesche Ausdrücke zu erstellen.  Im folgenden Beispiel wird die Verwendung von Vergleichsoperatoren in Verbindung mit einem logischen Operator veranschaulicht.  
  
 `x > y And x < 1000`  
  
 Im vorherigen Beispiel hängt der Wert des gesamten Ausdrucks von den Werten der Ausdrücke auf beiden Seiten des Operators `And` ab.  Wenn beide Ausdrücke `True` sind, ergibt der gesamte Ausdruck `True`.  Wenn einer der Ausdrücke `False` ist, ergibt der gesamte Ausdruck `False`.  
  
## Kurzschlussoperatoren  
 Das Verhalten der logischen Operatoren `AndAlso` und `OrElse` wird als *Kurzschluss* bezeichnet.  Ein Kurzschlussoperator wertet den linken Operanden zuerst aus.  Wenn der linke Operand den Wert des gesamten Ausdrucks bestimmt, wird die Ausführung des Programms fortgesetzt, ohne den rechten Ausdruck auszuwerten.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 [!CODE [VbVbalrOperators#89](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#89)]  
  
 Im vorangehenden Beispiel wertet der Operator den linken Ausdruck `45 < 12` aus.  Da der linke Ausdruck `False` ergibt, muss der gesamte logische Ausdruck `False` ergeben.  Das Programm überspringt daher die Ausführung des Codes im `If`\-Block, ohne den rechten Ausdruck `testFunction(3)` auszuwerten.  In diesem Beispiel wird `testFunction()` nicht aufgerufen, da der linke Ausdruck den gesamten Ausdruck als False bestimmt.  
  
 Wenn der linke Ausdruck in einem logischen Ausdruck mit `OrElse` den Wert `True` ergibt, wird entsprechend die Ausführung mit der nächsten Codezeile fortgesetzt, ohne den rechten Ausdruck auszuwerten, da der linke Ausdruck bereits den gesamten Ausdruck als True ausgewertet hat.  
  
### Vergleich mit Operatoren, die keine Kurzschlussoperatoren sind  
 Im Gegensatz dazu werden beide Seiten des logischen Operators ausgewertet, wenn die logischen Operatoren `And` und `Or` verwendet werden.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 [!CODE [VbVbalrOperators#90](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#90)]  
  
 Im vorherigen Beispiel wird `testFunction()` aufgerufen, obwohl der linke Ausdruck `False` ergibt.  
  
## Klammernausdrücke  
 Mit Klammern können Sie die Auswertungsreihenfolge von booleschen Ausdrücken steuern.  Ausdrücke in Klammern werden zuerst ausgewertet.  Bei mehrfachen Schachtelungsebenen werden die am tiefsten geschachtelten Ausdrücke vorrangig behandelt.  Innerhalb der Klammern wird die Auswertung entsprechend den Regeln der Operatorrangfolge vorgenommen.  Weitere Informationen finden Sie unter [Operator Precedence in Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md).  
  
## Siehe auch  
 [Logical and Bitwise Operators in Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)   
 [Value Comparisons](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)   
 [Statements](../../../../visual-basic/programming-guide/language-features/statements.md)   
 [Comparison Operators](../../../../visual-basic/language-reference/operators/comparison-operators.md)   
 [Efficient Combination of Operators](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/efficient-combination-of-operators.md)   
 [Operator Precedence in Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Boolean Data Type](../../../../visual-basic/language-reference/data-types/boolean-data-type.md)