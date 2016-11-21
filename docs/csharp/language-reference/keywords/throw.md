---
title: "throw (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "throw"
  - "throw_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "throw-Schlüsselwort [C#]"
  - "throw-Anweisung [C#]"
ms.assetid: 5ac4feef-4b1a-4c61-aeb4-61d549e5dd42
caps.latest.revision: 22
caps.handback.revision: 22
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# throw (C#-Referenz)
Mit der `throw`\-Anweisung wird das Auftreten einer außergewöhnlichen Situation oder Ausnahme während der Programmausführung signalisiert.  
  
## Hinweise  
 Die ausgelöste Ausnahme ist ein Objekt, dessen Klasse von <xref:System.Exception?displayProperty=fullName> abgeleitet wird, wie im folgenden Beispiel gezeigt.  
  
```  
class MyException : System.Exception {}  
// ...  
throw new MyException();  
```  
  
 Normalerweise wird die `throw`\-Anweisung mit `try-catch`\-Anweisungen oder `try-finally`\-Anweisungen verwendet.  Mit einer [throw](../../../csharp/language-reference/keywords/throw.md)\-Anweisung kann in einem `catch`\-Block die Ausnahme erneut ausgelöst werden, die vom `catch`\-Block abgefangen wurde.  In diesem Fall verwendet die [throw](../../../csharp/language-reference/keywords/throw.md)\-Anweisung keinen Operanden für die Ausnahme.  Weitere Informationen und Beispiele finden Sie unter [try\-catch](../../../csharp/language-reference/keywords/try-catch.md) und [Gewusst wie: Explizites Auslösen von Ausnahmen](../Topic/How%20to:%20Explicitly%20Throw%20Exceptions.md).  
  
## Beispiel  
 In diesem Beispiel wird veranschaulicht, wie mit der `throw`\-Anweisung eine Ausnahme ausgelöst wird.  
  
 [!CODE [csrefKeywordsExceptions#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsExceptions#5)]  
  
## Codebeispiel  
 Weitere Informationen finden Sie in den Beispielen in [try\-catch](../../../csharp/language-reference/keywords/try-catch.md) und [Gewusst wie: Explizites Auslösen von Ausnahmen](../Topic/How%20to:%20Explicitly%20Throw%20Exceptions.md).  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [try\-catch](../../../csharp/language-reference/keywords/try-catch.md)   
 [Die try\-, catch\- und throw\-Anweisung in C\+\+](../../../csharp/language-reference/keywords/try-catch.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Ausnahmebehandlungsanweisungen](../../../csharp/language-reference/keywords/exception-handling-statements.md)   
 [Gewusst wie: Explizites Auslösen von Ausnahmen](../Topic/How%20to:%20Explicitly%20Throw%20Exceptions.md)