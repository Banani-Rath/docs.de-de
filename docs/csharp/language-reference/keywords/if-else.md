---
title: "if-else (C#-Referenz) | Microsoft Docs"
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
  - "if_CSharpKeyword"
  - "else"
  - "else_CSharpKeyword"
  - "if"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "else-Schlüsselwort [C#]"
  - "if-Schlüsselwort [C#]"
ms.assetid: d9a1d562-8cf5-4bd4-9ba7-8ad970cd25b2
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# if-else (C#-Referenz)
Eine `if`\-Anweisung ermittelt, welche Anweisung basierend auf dem Wert eines `Boolean`Ausdrucks auszuführen ist. Im folgenden Beispiel wird die `Boolean`Variable `result` auf `true` festgelegt und dann in der `if`Anweisung überprüft. Die Ausgabe lautet `The condition is true`.  
  
 [!CODE [csrefKeywordsSelection#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#1)]  
  
 Die können die Beispiele in diesem Thema ausführen, indem Sie sie in die `Main`\-Methode einer Konsolenanwendung platzieren.  
  
 Eine `if`\-Anweisung in C\# kann zwei Formen annehmen, wie im folgenden Beispiel gezeigt.  
  
```c#  
  
// if-else statement if (condition) { then-statement; } else { else-statement; } // Next statement in the program. // if statement without an else if (condition) { then-statement; } // Next statement in the program.  
```  
  
 In einer `if-else`\-Anweisung wird, wenn `condition` zu true ausgewertet wird, `then-statement` ausgeführt. Wenn `condition` false ist, wird `else-statement` ausgeführt. Da `condition` nicht gleichzeitig true und false sein kann, können `then-statement` und `else-statement` einer `if-else`\-Anweisung niemals beide ausgeführt werden. Nachdem `then-statement` oder `else-statement` ausgeführt wurde, wird die Steuerung an die `if`\-Anweisung übergeben.  
  
 In einer `if`\-Anweisung, die keine `else`\-Anweisung enthält, wird, wenn `condition` true ist, `then-statement` ausgeführt. Wenn `condition` false ist, wird die Steuerung an die nächste Anweisung nach der `if`Anweisung übergeben.  
  
 Sowohl `then-statement` als auch `else-statement` können aus einer einzelnen Anweisung oder mehreren in Klammern eingeschlossenen Anweisungen bestehen \(`{}`\). Bei einer Anweisung sind die Klammern optional, sie werden aber empfohlen.  
  
 Die Anweisung bzw. die Anweisungen in `then-statement` und `else-statement` können von einer beliebigen Art sein und eine weitere `if`Anweisung enthalten, die in der ursprünglichen `if`\-Anweisung geschachtelt ist. In geschachtelten `if`Anweisungen gehört jede `else`\-Klausel zur letzten `if`\-Anweisung, die nicht über eine zugehörige `else`\-Anweisung verfügt. Im folgenden Beispiel wird `Result1` angezeigt, wenn `m > 10` und `n > 20` zu true ausgewertet werden. Wenn `m > 10` true ist, `n > 20` hingegen false, wird `Result2` angezeigt.  
  
 [!CODE [csrefKeywordsSelection#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#2)]  
  
 Wenn stattdessen `Result2` angezeigt werden soll, wenn `(m > 10)` false ist, können Sie diese Zuordnung mithilfe von Klammern festlegen, um den Beginn und das Ende der geschachtelten `if`Anweisung anzugeben, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csrefKeywordsSelection#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#3)]  
  
 `Result2` wird angezeigt, wenn die Bedingung `(m > 10)` zu false ausgewertet wird.  
  
## Beispiel  
 Im folgenden Beispiel geben Sie ein Zeichen über die Tastatur ein. Das Programm verwendet eine geschachtelte `if`\-Anweisung, um zu bestimmen, ob das eingegebene Zeichen ein alphabetisches Zeichen ist. Wenn das eingegebene Zeichen ein alphabetisches Zeichen ist, überprüft das Programm, ob das eingegebene Zeichen in Groß\- oder in Kleinschreibung ist. In beiden Fällen wird eine Meldung angezeigt.  
  
 [!CODE [csrefKeywordsSelection#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#4)]  
  
## Beispiel  
 Sie können eine `if`Anweisung auch in einem else\-Block schachteln, wie der folgende Codeausschnitt zeigt. Im Beispiel werden `if`Anweisungen in zwei else\-Blocks und einem then\-Block geschachtelt. In den Kommentaren ist angegeben, welche Bedingungen in jedem Block true oder false sind.  
  
 [!CODE [csrefKeywordsSelection#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#5)]  
  
## Beispiel  
 Im folgenden Beispiel wird bestimmt, ob ein eingegebenes Zeichen ein Kleinbuchstabe, ein Großbuchstabe oder eine Zahl ist. Wenn alle drei Bedingungen false sind, ist das Zeichen kein alphanumerisches Zeichen. Das Beispiel zeigt für jeden Fall eine Meldung an.  
  
 [!CODE [csrefKeywordsSelection#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#6)]  
  
 So, wie eine Anweisung im else\-Block oder then\-Block jede beliebige Anweisung sein kann, können Sie für die Bedingungen einen beliebigen gültigen booleschen Ausdruck verwenden. Sie können logische Operatoren wie [&&](../../../csharp/language-reference/operators/conditional-and-operator.md), [&](../../../csharp/language-reference/operators/and-operator.md), [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md), [&#124;](../../../csharp/language-reference/operators/or-operator.md) und [\!](../../../csharp/language-reference/operators/logical-negation-operator.md) verwenden, um Verbundbedingungen zu erstellen. Der folgende Code enthält Beispiele.  
  
```c#  
// NOT bool result = true; if (!result) { Console.WriteLine("The condition is true (result is false)."); } else { Console.WriteLine("The condition is false (result is true)."); } // Short-circuit AND int m = 9; int n = 7; int p = 5; if (m >= n && m >= p) { Console.WriteLine("Nothing is larger than m."); } // AND and NOT if (m >= n && !(p > m)) { Console.WriteLine("Nothing is larger than m."); } // Short-circuit OR if (m > n || m > p) { Console.WriteLine("m isn't the smallest."); } // NOT and OR m = 4; if (!(m >= n || m >= p)) { Console.WriteLine("Now m is the smallest."); } // Output: // The condition is false (result is true). // Nothing is larger than m. // Nothing is larger than m. // m isn't the smallest. // Now m is the smallest.  
```  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Operator ?:](../../../csharp/language-reference/operators/conditional-operator.md)   
 [if\-else\-Anweisung \(C\+\+\)](/visual-cpp/cpp/if-else-statement-cpp)   
 [switch](../../../csharp/language-reference/keywords/switch.md)