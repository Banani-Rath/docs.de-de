---
title: "How to: Define a Conversion Operator (Visual Basic) | Microsoft Docs"
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
  - "procedures, defining"
  - "operators [Visual Basic], defining"
  - "procedures, operator"
  - "operators [Visual Basic], overloading"
  - "return values, Operator procedures"
  - "operator overloading"
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Define a Conversion Operator (Visual Basic)
Wenn Sie eine Klasse oder Struktur definiert haben, können Sie für die Konvertierung vom Typ der Klasse bzw. Struktur in einen anderen Datentyp \(z. B. `Integer`, `Double` oder `String`\) einen Typkonvertierungsoperator definieren.  
  
 Definieren Sie die Typkonvertierung als eine [CType\-Funktion](../../../../visual-basic/language-reference/functions/ctype-function.md)\-Prozedur innerhalb der Klasse oder der Struktur.  Alle Konvertierungsprozeduren müssen `Public Shared` sein, und jede muss entweder [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) oder [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md) angeben.  
  
 Das Definieren eines Operators für eine Klasse oder Struktur wird auch als *Überladen* bezeichnet.  
  
## Beispiel  
 Im folgenden Beispiel werden Operatoren für die Konvertierung zwischen einer Struktur mit dem Namen `digit` und einem `Byte` definiert.  
  
 [!CODE [VbVbcnProcedures#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#27)]  
  
 Sie können die Struktur `digit` mit dem folgenden Code testen.  
  
 [!CODE [VbVbcnProcedures#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#28)]  
  
## Siehe auch  
 [Operator Procedures](../../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)   
 [How to: Define an Operator](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)   
 [How to: Call an Operator Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-call-an-operator-procedure.md)   
 [How to: Use a Class that Defines Operators](../../../../visual-basic/programming-guide/language-features/procedures/how-to-use-a-class-that-defines-operators.md)   
 [Operator Statement](../../../../visual-basic/language-reference/statements/operator-statement.md)   
 [Structure Statement](../../../../visual-basic/language-reference/statements/structure-statement.md)   
 [How to: Declare a Structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)   
 [Implicit and Explicit Conversions](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)   
 [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)