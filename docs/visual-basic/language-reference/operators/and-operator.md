---
title: "And Operator (Visual Basic) | Microsoft Docs"
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
  - "vb.And"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "operators [Visual Basic], bitwise"
  - "logical conjunction"
  - "bitwise AND operator [Visual Basic]"
  - "conjunction operator"
  - "And operator [Visual Basic]"
  - "bitwise operators, AND operator"
  - "operators [Visual Basic], conjunction"
  - "bitwise comparison"
ms.assetid: 2ea711f3-439a-4c7c-9e3a-1ffe3b0d6046
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# And Operator (Visual Basic)
Führt eine logische Konjunktion zweier `Boolean`\-Ausdrücke oder eine bitweise Konjunktion zweier numerischer Ausdrücke aus.  
  
## Syntax  
  
```  
  
result = expression1 And expression2  
```  
  
## Teile  
 `result`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  Bei booleschen Vergleichen ist `result` die logische Konjunktion von zwei `Boolean`\-Werten.  Bei bitweisen Operationen ist `result` ein numerischer Wert, der die bitweise Konjunktion von zwei numerischen Bitmustern darstellt.  
  
 `expression1`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  
  
 `expression2`  
 Erforderlich.  Ein beliebiger `Boolean`\-Ausdruck oder numerischer Ausdruck.  
  
## Hinweise  
 Bei booleschen Vergleichen ist `result` dann und nur dann `True`, wenn sowohl`expression1` als auch `expression2` zu `True` ausgewertet werden.  Die folgende Tabelle veranschaulicht, wie `result` bestimmt wird.  
  
|Wert von `expression1`|Und `expression2` gleich|hat `result` den Wert|  
|----------------------------|------------------------------|---------------------------|  
|`True`|`True`|`True`|  
|`True`|`False`|`False`|  
|`False`|`True`|`False`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  In einem booleschen Vergleich wertet der Operator `And` immer beide Ausdrücke aus, wobei u. U. Prozeduraufrufe ausgeführt werden können.  Der [AndAlso Operator](../../../visual-basic/language-reference/operators/andalso-operator.md) führt *Kurzschlussoperationen* aus. Das bedeutet, dass `expression2` nicht ausgewertet wird, wenn `expression1``False` ist.  
  
 Wenn der Operator `And` auf numerische Werte angewendet wird, werden identisch positionierte Bits in zwei numerischen Ausdrücken bitweise verglichen. Das entsprechende Bit wird entsprechend der folgenden Tabelle in `result` eingesetzt:  
  
|Wenn Bit in `expression1` gleich|Und Bit in `expression2` gleich|Dann ist das Bit in `result` gleich|  
|--------------------------------------|-------------------------------------|-----------------------------------------|  
|1|1|1|  
|1|0|0|  
|0|1|0|  
|0|0|0|  
  
> [!NOTE]
>  Da die logischen und bitweisen Operatoren einen niedrigeren Rang als andere arithmetische und relationale Operatoren haben, müssen alle bitweisen Operationen in runde Klammern gesetzt werden, um präzise Ergebnisse zu gewährleisten.  
  
## Datentypen  
 Wenn die Operanden aus einem `Boolean`\-Ausdruck und einem numerischen Ausdruck bestehen, konvertiert Visual Basic den `Boolean`\-Ausdruck in einen numerischen Wert \(–1 für `True` und 0 für `False`\) und führt eine bitweise Operation aus.  
  
 Bei einem Vergleich von booleschen Ausdrücken ist der Datentyp des Ergebnisses `Boolean`.  Bei einem bitweisen Vergleich ist der Datentyp des Ergebnisses ein numerischer Typ, der für die Datentypen von `expression1` und `expression2` geeignet ist.  Siehe die Tabelle "Relationale und bitweise Vergleiche" in [Data Types of Operator Results](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
> [!NOTE]
>  Der Operator `And` kann *überladen* werden. Das bedeutet, dass eine Klasse oder Struktur sein Verhalten neu definiert, wenn ein Operand den Typ dieser Klasse oder Struktur aufweist.  Wenn Sie diesen Operator im Code auf eine solche Klasse oder Struktur anwenden, sollten Sie auf jeden Fall sein neu definiertes Verhalten verstehen.  Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## Beispiel  
 In diesem Beispiel wird mit dem Operator `And` eine logische Konjunktion zweier Ausdrücke ausgeführt.  Das Ergebnis ist ein `Boolean`\-Wert, der darstellt, ob beide Ausdrücke `True` sind.  
  
 [!CODE [VbVbalrOperators#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#22)]  
  
 Im vorangehenden Beispiel werden die Ergebnisse `True` bzw. `False` berechnet.  
  
## Beispiel  
 Im folgenden Beispiel wird mit dem Operator `And` eine logische Konjunktion einzelner Bits zweier numerischer Ausdrücke ausgeführt.  Das Bit im Ergebnismuster wird gesetzt, wenn die beiden entsprechenden Bits in den Operanden auf 1 gesetzt sind.  
  
 [!CODE [VbVbalrOperators#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#23)]  
  
 Im vorangehenden Beispiel werden die Ergebnisse 8, 2 bzw. 0 berechnet.  
  
## Siehe auch  
 [Logical\/Bitwise Operators](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)   
 [Operator Precedence in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)   
 [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)   
 [AndAlso Operator](../../../visual-basic/language-reference/operators/andalso-operator.md)   
 [Logical and Bitwise Operators in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)