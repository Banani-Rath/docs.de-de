---
title: "Iterator (Visual Basic) | Microsoft Docs"
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
  - "vb.Iterator"
helpviewer_keywords: 
  - "Iterator keyword [Visual Basic]"
ms.assetid: 69cb0b04-ac87-49d0-bcfe-810c0d60daff
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Iterator (Visual Basic)
Gibt an, dass eine Funktion oder ein `Get` Accessor ein Iterator ist.  
  
## Hinweise  
 Ein *Iterator* führt eine benutzerdefinierte Iteration durch eine Auflistung aus.  Ein Iterator verwendet die [Ertrag](../../../visual-basic/language-reference/statements/yield-statement.md)\-Anweisung, um jedes einzelne Element in der Auflistung zurückgegeben werden soll.  Wenn eine `Yield`\-Anweisung erreicht wird, wird der aktuelle Position im Code beibehalten.  Die Ausführung wird von diesem Speicherort beim nächsten Mal neu gestartet, dass die Iterator Funktion aufgerufen wird.  
  
 Ein Iterator kann als Funktion oder als `Get` Accessor einer Eigenschaftendefinition implementiert werden.  Der `Iterator`\-Modifizierer wird in der Deklaration der Iterator `Get`\-Funktion oder des Accessors.  
  
 Sie rufen den Iterator im Clientcode an, indem Sie [For Each...Next\-Anweisung](../../../visual-basic/language-reference/statements/for-each-next-statement.md) verwenden.  
  
 Der Rückgabetyp einer Funktion oder eines `Get` Iterator <xref:System.Collections.IEnumerable> Accessors kann, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator> oder <xref:System.Collections.Generic.IEnumerator%601> sein.  
  
 Ein Iterator `ByRef` darf keine Parameter enthalten.  
  
 Ein Iterator kann nicht in einem Ereignis in einem Instanzenkonstruktor, in einem statischen Konstruktor oder Destruktor in einem statischen auftreten.  
  
 Ein Iterator kann eine anonyme Funktion sein.  Weitere Informationen finden Sie unter [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
 Weitere Informationen zu Iteratoren finden Sie unter [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Verwendung  
 Der `Iterator`\-Modifizierer kann in folgenden Kontexten verwendet werden:  
  
-   [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md)  
  
-   [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md)  
  
## Beispiel  
 Im folgenden Beispiel wird ein Iterator für Reservierungen.  Die Iterator `Yield`\-Funktion ist eine Anweisung, die innerhalb einer Schleife [Weitere… Next](../../../visual-basic/language-reference/statements/for-next-statement.md) ist.  Jede Iteration des Anweisungstexts [Für jedes](../../../visual-basic/language-reference/statements/for-each-next-statement.md) in `Main` erstellt einen Aufruf der `Power` Iterator für Reservierungen.  Jeder Aufruf der Iterator zur nächsten wechselt das Feature für die Ausführung der Anweisung über `Yield`, die während der nächsten Iteration der Schleife `For…Next` auftritt.  
  
 [!CODE [VbVbalrStatements#98](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#98)]  
  
## Beispiel  
 Im folgenden Beispiel wird ein `Get` Accessor, der einen Iterator ist.  Der `Iterator`\-Modifizierer ist in die Eigenschaftendeklaration.  
  
 [!CODE [VbVbalrStatements#99](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#99)]  
  
 Weitere Beispiele finden Sie unter [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Siehe auch  
 <xref:System.Runtime.CompilerServices.IteratorStateMachineAttribute>   
 [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)   
 [Yield\-Anweisung](../../../visual-basic/language-reference/statements/yield-statement.md)