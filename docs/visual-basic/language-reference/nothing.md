---
title: "Nothing (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "Nothing"
  - "vb.Nothing"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Nothing keyword"
  - "Nothing keyword, syntax"
ms.assetid: 06176e2d-bbf7-4a37-afaa-a86ad21ee99f
caps.latest.revision: 31
caps.handback.revision: 31
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Nothing (Visual Basic)
Stellt den Standardwert jedes beliebigen Datentyps dar.  Bei Verweistypen lautet der Standardwert der `null` Reference.  Für Werttypen Der Standardwert hängt davon ab, ob der Werttyp NULL\-Werte zulässig sind.  
  
> [!NOTE]
>  Für nicht auf NULL festlegbare Werttypen unterscheiden sich `Nothing` in Visual Basic aus `null` in C\#.  Wenn Sie in Visual Basic in einer Variablen eines Werttyps keine NULL\-Werte zulassen auf `Nothing`, die Variable auf den Standardwert für den deklarierten Typ festgelegt werden.  In C\# `null`Wenn Sie eine Variable eines nicht auf NULL festlegbare Werttyp zuweisen, tritt ein Kompilierungsfehler auf.  
  
## Hinweise  
 `Nothing` stellt den Standardwert eines Datentyps dar.  Der Standardwert hängt davon ab, ob die Variable von einem Werttyp oder ein Verweistyp ist.  
  
 Eine Variable eines *Werttyps* enthält den Wert direkt.  Werttypen umfassen alle numerischen Datentypen `Boolean`, `Char`, `Date`, alle Strukturen und Enumerationen.  Eine Variable eines *Referenztyps* enthält einen Verweis auf eine Instanz eines Objekts im Arbeitsspeicher.  Verweistypen umfassen Klassen, Arrays, \- Delegaten und die Zeichenfolgen.  Weitere Informationen finden Sie unter [Value Types and Reference Types](../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md).  
  
 Wenn eine Variable von einem Werttyp ist, hängt das Verhalten von `Nothing` davon ab, ob die Variable von einem Datentyp NULL\-Werte zulässt.  Um einen Werttyp, der auf NULL festgelegt werden `?` darzustellen, fügen Sie einen Typnamen dem Modifizierer hinzu.  Das Zuweisen von `Nothing` auf eine Variable, die NULL\-Werte zulassen `null`zu legt den Wert fest.  Weitere Informationen und Beispiele finden Sie unter [Nullable Value Types](../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md).  
  
 Wenn eine Variable von einem Werttyp ist, der keine NULL\-Werte zulässig sind, wird das Zuweisen von `Nothing` an den Standardwert für den deklarierten Typ fest.  Wenn der Typ Variablenmember enthält, werden für alle die jeweiligen Standardwerte festgelegt.  Im folgenden Beispiel wird dieses für skalare Typen veranschaulicht.  
  
 [!CODE [VbVbalrKeywords#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#7)]  
  
 Wenn eine Variable von einem Referenztyp ist, und weist `Nothing` in den variablen oder legt sie auf einen `null` Verweis vom Typ der Variablen zu.  Eine Variable, die einem `null` Verweis festgelegt wird, ist keinem Objekt zugeordnet.  Das folgende Beispiel veranschaulicht dies.  
  
 [!CODE [VbVbalrKeywords#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#8)]  
  
 Beim Überprüfen, ob eine Bezugs\- NULL\-Werte zulässt \(oder Werttyp\) \- Variable `null`ist, verwenden Sie nicht `= Nothing` oder `<> Nothing`.  Immer Verwendung `Is Nothing` oder `IsNot Nothing`.  
  
 Für Zeichenfolgen in Visual Basic ist die leere Zeichenfolge `Nothing`.  Daher ist `"" = Nothing` true.  
  
 Im folgenden Beispiel werden Vergleiche mithilfe des `Is`\-Operators und des `IsNot`\-Operators veranschaulicht.  
  
 [!CODE [VbVbalrKeywords#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#9)]  
  
 Wenn Sie eine Variable ohne Verwendung einer `As`\-Klausel deklarieren und auf `Nothing` festlegen, ist die Variable vom Typ `Object`.  Ein Beispiel hierfür ist `Dim something = Nothing`.  In diesem Fall tritt ein Kompilierungsfehler auf, wenn `Option Strict` aktiviert ist und `Option Infer` deaktiviert ist.  
  
 Wenn `Nothing` einer Objektvariablen zugewiesen wird, verweist diese Variable nicht mehr auf eine Objektinstanz.  Wenn die Variable zuvor auf eine Instanz verwies, wird mit `Nothing` die Instanz selbst nicht beendet.  Die Beendigung der Instanz sowie die Freigabe des benötigten Speicherplatzes und der benötigten Systemressourcen erfolgt erst dann, wenn der Garbage Collector \(GC\) keine aktiven Verweise mehr findet.  
  
 `Nothing` unterscheidet sich vom <xref:System.DBNull>\-Objekt, das eine nicht initialisierte Variante oder eine nicht vorhandene Datenbankspalte darstellt.  
  
## Siehe auch  
 [Dim Statement](../../visual-basic/language-reference/statements/dim-statement.md)   
 [Object Lifetime: How Objects Are Created and Destroyed](../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)   
 [Lifetime in Visual Basic](../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)   
 [Is Operator](../../visual-basic/language-reference/operators/is-operator.md)   
 [IsNot Operator](../../visual-basic/language-reference/operators/isnot-operator.md)   
 [Nullable Value Types](../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)