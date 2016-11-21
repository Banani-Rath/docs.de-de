---
title: "How to: Create a Lambda Expression (Visual Basic) | Microsoft Docs"
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
  - "lambda expressions [Visual Basic]"
  - "expressions [Visual Basic], lambda"
ms.assetid: 3279bd5c-80f7-410a-a7ba-f7085ed36aa5
caps.latest.revision: 27
caps.handback.revision: 27
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create a Lambda Expression (Visual Basic)
Ein *Lambda\-Ausdruck* ist eine Funktion oder Unterroutine, die keinen Namen aufweist.  Lambda\-Ausdrücke können an allen Stellen verwendet werden, an denen ein Delegattyp gültig ist.  
  
### So erstellen Sie eine einzeilige Funktion mit einem Lambda\-Ausdruck  
  
1.  Geben Sie in einer Situation, in der ein Delegattyp verwendet werden kann, wie im folgenden Beispiel veranschaulicht, das Schlüsselwort `Function` ein:  
  
     `Dim add1 =`   `Function`  
  
2.  Geben Sie direkt nach `Function` in Klammern die Parameter der Funktion ein.  Beachten Sie, dass nach `Function` kein Name festgelegt wird.  
  
     `Dim add1 = Function`   `(num As Integer)`  
  
3.  Geben Sie nach der Parameterliste einen einzelnen Ausdruck als Text der Funktion ein.  Der Wert, den der Ausdruck ergibt, wird von der Funktion zurückgegeben.  Sie verwenden keine `As`\-Klausel, um den Rückgabetyp festzulegen.  
  
     [!CODE [VbVbalrLambdas#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#1)]  
  
     Sie rufen den Lambda\-Ausdruck auf, indem Sie ein Ganzzahlargument übergeben.  
  
     [!CODE [VbVbalrLambdas#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#2)]  
  
4.  Das gleiche Ergebnis wird auch in folgendem Beispiel erreicht:  
  
     [!CODE [VbVbalrLambdas#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#3)]  
  
### So erstellen Sie eine einzeilige Unterroutine mit einem Lambda\-Ausdruck  
  
1.  Geben Sie in einer Situation, in der ein Delegattyp verwendet werden kann, wie im folgenden Beispiel veranschaulicht, das Schlüsselwort `Sub` ein:  
  
     `Dim add1 =`   `Sub`  
  
2.  Geben Sie direkt nach `Sub` in Klammern die Parameter der Unterroutine ein.  Beachten Sie, dass nach `Sub` kein Name festgelegt wird.  
  
     `Dim add1 = Sub`   `(msg As String)`  
  
3.  Geben Sie nach der Parameterliste eine einzelne Anweisung als Text der Unterroutine ein.  
  
     [!CODE [VbVbalrLambdas#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#17)]  
  
     Sie rufen den Lambda\-Ausdruck auf, indem Sie ein Zeichenfolgenargument übergeben.  
  
     [!CODE [VbVbalrLambdas#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#18)]  
  
### So erstellen Sie eine mehrzeilige Funktion mit einem Lambda\-Ausdruck  
  
1.  Geben Sie in einer Situation, in der ein Delegattyp verwendet werden kann, wie im folgenden Beispiel veranschaulicht, das Schlüsselwort `Function` ein:  
  
     `Dim add1 =`   `Function`  
  
2.  Geben Sie direkt nach `Function` in Klammern die Parameter der Funktion ein.  Beachten Sie, dass nach `Function` kein Name festgelegt wird.  
  
     `Dim add1 = Function`   `(index As Integer)`  
  
3.  Drücken Sie die EINGABETASTE.  Die `End Function`\-Anweisung wird automatisch hinzugefügt.  
  
4.  Fügen Sie im Text der Funktion den folgenden Code hinzu, um einen Ausdruck zu erstellen und den Wert zurückzugeben.  Sie verwenden keine `As`\-Klausel, um den Rückgabetyp festzulegen.  
  
     [!CODE [VbVbalrLambdas#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#19)]  
  
     Sie rufen den Lambda\-Ausdruck auf, indem Sie ein Ganzzahlargument übergeben.  
  
     [!CODE [VbVbalrLambdas#20](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#20)]  
  
### So erstellen Sie eine mehrzeilige Unterroutine mit einem Lambda\-Ausdruck  
  
1.  Geben Sie in einer Situation, in der ein Delegattyp verwendet werden kann, wie im folgenden Beispiel veranschaulicht, das Schlüsselwort `Sub` ein:  
  
     `Dim add1 =`   `Sub`  
  
2.  Geben Sie direkt nach `Sub` in Klammern die Parameter der Unterroutine ein.  Beachten Sie, dass nach `Sub` kein Name festgelegt wird.  
  
     `Dim add1 = Sub`  `(msg As String)`  
  
3.  Drücken Sie die EINGABETASTE.  Die `End Sub`\-Anweisung wird automatisch hinzugefügt.  
  
4.  Fügen Sie im Text der Funktion den folgenden Code hinzu, der beim Aufrufen der Unterroutine ausgeführt werden soll.  
  
     [!CODE [VbVbalrLambdas#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#21)]  
  
     Sie rufen den Lambda\-Ausdruck auf, indem Sie ein Zeichenfolgenargument übergeben.  
  
     [!CODE [VbVbalrLambdas#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#22)]  
  
## Beispiel  
 Eine häufige Verwendung von Lambda\-Ausdrücken ist das Definieren einer Funktion, die als Argument für einen Parameter vom Typ `Delegate` übergeben werden kann.  Im folgenden Beispiel wird von der <xref:System.Diagnostics.Process.GetProcesses%2A>\-Methode ein Array der Prozesse zurückgegeben, die auf dem lokalen Computer ausgeführt werden.  Für die <xref:System.Linq.Enumerable.Where%2A>\-Methode der <xref:System.Linq.Enumerable>\-Klasse ist ein `Boolean`\-Delegat als Argument erforderlich.  Zu diesem Zweck wird im Beispiel der Lambda\-Ausdruck verwendet.  Er gibt `True` für alle Prozesse mit nur einem Thread zurück, und diese werden in der `filteredList` ausgewählt.  
  
 [!CODE [VbVbalrLambdas#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#10)]  
  
 Das vorherige Beispiel ist äquivalent zu folgendem, in [!INCLUDE[vbteclinqext](../../../../csharp/getting-started/includes/vbteclinqext_md.md)]\-Syntax geschriebenem Code:  
  
 [!CODE [VbVbalrLambdas#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#11)]  
  
## Siehe auch  
 <xref:System.Linq.Enumerable>   
 [Lambda Expressions](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)   
 [Function Statement](../../../../visual-basic/language-reference/statements/function-statement.md)   
 [Sub Statement](../../../../visual-basic/language-reference/statements/sub-statement.md)   
 [Delegates](../../../../visual-basic/programming-guide/language-features/delegates/delegates.md)   
 [How to: Pass Procedures to Another Procedure in Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)   
 [Delegate Statement](../../../../visual-basic/language-reference/statements/delegate-statement.md)   
 [Introduction to LINQ in Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)