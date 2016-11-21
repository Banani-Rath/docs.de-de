---
title: "Or Operator (Visual Basic) | Microsoft Docs"
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
  - "vb.Or"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Or operator"
  - "operators [Visual Basic], bitwise"
  - "inclusive Or operator"
  - "bitwise operators, OR operator"
  - "Or keyword"
  - "operators [Visual Basic], inclusive or"
  - "operators [Visual Basic], disjunction"
  - "bitwise comparison"
  - "logical disjunction"
  - "disjunction operator"
ms.assetid: 41ed6905-bf3d-468a-9e3b-03c10d461891
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Or Operator (Visual Basic)
Führt eine logische Disjunktion zweier `Boolean`\-Ausdrücke oder eine bitweise Disjunktion zweier numerischer Ausdrücke aus.  
  
## Syntax  
  
```  
  
result = expression1 Or expression2  
```  
  
## Teile  
 `result`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  Bei einem `Boolean`\-Vergleich ist `result` die inklusive logische Disjunktion von zwei `Boolean`\-Werten.  Bei bitweisen Operationen ist `result` ein numerischer Wert, der die inklusive bitweise Disjunktion von zwei numerischen Bitmustern darstellt.  
  
 `expression1`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  
  
 `expression2`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  
  
## Hinweise  
 Bei einem `Boolean`\-Vergleich ist `result` nur dann `False`, wenn `expression1` und `expression2` `False` ergeben.  Die folgende Tabelle veranschaulicht, wie `result` bestimmt wird.  
  
|Wert von `expression1`|Und `expression2` gleich|hat `result` den Wert|  
|----------------------------|------------------------------|---------------------------|  
|`True`|`True`|`True`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  In einem `Boolean`\-Vergleich wertet der Operator `Or` stets beide Ausdrücke aus; dabei werden unter Umständen auch Prozeduraufrufe ausgeführt.  Der [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md) führt *Kurzschlussoperationen* aus. Dies bedeutet, dass `expression2` nicht ausgewertet wird, wenn `expression1` `True` ist.  
  
 Bei bitweisen Operationen führt der Operator `Or` einen bitweisen Vergleich von identisch positionierten Bits in zwei numerischen Ausdrücken aus und legt das entsprechende Bit in `result` entsprechend der folgenden Tabelle fest.  
  
|Wenn Bit in `expression1` gleich|Und Bit in `expression2` gleich|Dann ist das Bit in `result` gleich|  
|--------------------------------------|-------------------------------------|-----------------------------------------|  
|1|1|1|  
|1|0|1|  
|0|1|1|  
|0|0|0|  
  
> [!NOTE]
>  Da die logischen und bitweisen Operatoren einen niedrigeren Rang als andere arithmetische und relationale Operatoren haben, müssen alle bitweisen Operationen in Klammern platziert werden, damit eine genaue Ausführung gewährleistet ist.  
  
## Datentypen  
 Wenn die Operanden aus einem `Boolean`\-Ausdruck und einem numerischen Ausdruck bestehen, konvertiert Visual Basic den `Boolean`\-Ausdruck in einen numerischen Wert \(–1 für `True` und 0 für `False`\) und führt eine bitweise Operation aus.  
  
 Bei einem `Boolean`\-Vergleich ist der Datentyp des Ergebnisses `Boolean`.  Bei einem bitweisen Vergleich ist der Datentyp des Ergebnisses ein numerischer Typ, der für die Datentypen von `expression1` und `expression2` geeignet ist.  Siehe die Tabelle "Relationale und bitweise Vergleiche" in [Data Types of Operator Results](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
## Überladen  
 Der Operator `Or` kann *überladen* werden. Das bedeutet, dass eine Klasse oder Struktur sein Verhalten neu definiert, wenn ein Operand den Typ dieser Klasse oder Struktur aufweist.  Wenn Sie diesen Operator im Code auf eine solche Klasse oder Struktur anwenden, sollten Sie auf jeden Fall sein neu definiertes Verhalten verstehen.  Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Beispiel  
 Im folgenden Beispiel wird mit dem Operator `Or` an zwei Ausdrücken eine inklusive logische Disjunktion ausgeführt.  Das Ergebnis ist ein `Boolean`\-Wert, der darstellt, ob einer der beiden Ausdrücke `True` ist.  
  
 [!CODE [VbVbalrOperators#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#35)]  
  
 Durch das vorangehende Beispiel werden die Ergebnisse `True`, `True` bzw. `False` erzeugt.  
  
## Beispiel  
 In diesem Beispiel wird mit dem Operator `Or` eine inklusive logische Disjunktion der einzelnen Bits von zwei numerischen Ausdrücken ausgeführt.  Das Bit im Ergebnismuster wird aktiviert, wenn eines der beiden entsprechenden Bits in den Operanden auf 1 gesetzt wird.  
  
 [!CODE [VbVbalrOperators#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#36)]  
  
 Durch das vorangehende Beispiel werden die Ergebnisse 10, 14 bzw. 14 erzeugt.  
  
## Siehe auch  
 [Logical\/Bitwise Operators](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md)   
 [Logical and Bitwise Operators in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)