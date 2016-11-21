---
title: "yield (C#-Referenz) | Microsoft Docs"
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
  - "yield"
  - "yield_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "yield-Schlüsselwort [C#]"
ms.assetid: 1089194f-9e53-46a2-8642-53ccbe9d414d
caps.latest.revision: 46
caps.handback.revision: 46
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# yield (C#-Referenz)
Wenn Sie das `yield`\-Schlüsselwort in einer Anweisung verwenden, geben Sie damit an, dass die Methode, der Operator oder der `get`\-Accessor, in dem es vorkommt, ein Iterator ist.  Wird ein Iterator mithilfe von `yield` definiert, ist eine explizite zusätzliche Klasse \(die Klasse, die den Zustand für eine Enumeration enthält, siehe beispielsweise <xref:System.Collections.Generic.IEnumerator%601>\) nicht erforderlich, wenn Sie das <xref:System.Collections.IEnumerable>\-Muster und das <xref:System.Collections.IEnumerator>\-Muster für einen benutzerdefinierten Auflistungstyp implementieren.  
  
 Im folgenden Beispiel werden zwei Formen der `yield`\-Anweisung gezeigt.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
## Hinweise  
 Sie verwenden eine `yield return`\-Anweisung, um jedes Element einzeln zurückzugeben.  
  
 Sie erzeugen eine Iteratormethode, indem Sie eine [foreach](../../../csharp/language-reference/keywords/foreach-in.md)\-Anweisung oder eine LINQ\-Abfrage verwenden.  Jede Iteration der `foreach`\-Schleife ruft die Iteratormethode auf.  Wenn eine `yield return`\-Anweisung im Iterator erreicht wird, wird ein `expression`\-Ausdruck zurückgegeben, und die aktuelle Position im Code wird beibehalten.  Wenn die Iteratorfunktion das nächste Mal aufgerufen wird, wird die Ausführung von dieser Position neu gestartet.  
  
 Sie verwenden eine `yield break`\-Anweisung, um die Iteration zu beenden.  
  
 Weitere Informationen zu Iteratoren finden Sie unter [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Iteratormethoden und get\-Accessoren  
 Die Deklaration eines Iterators muss die folgenden Anforderungen erfüllen:  
  
-   Der Rückgabetyp muss <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator> oder <xref:System.Collections.Generic.IEnumerator%601> sein.  
  
-   Die Deklaration darf nicht über [ref](../../../csharp/language-reference/keywords/ref.md)\- oder [out](../../../csharp/language-reference/keywords/out.md)\-Parameter verfügen.  
  
 Der `yield`\-Typ eines Iterators, der <xref:System.Collections.IEnumerable> oder <xref:System.Collections.IEnumerator> zurückgibt, ist `object`.  Wenn der Iterator <xref:System.Collections.Generic.IEnumerable%601> oder <xref:System.Collections.Generic.IEnumerator%601> zurückgibt, ist eine implizite Konvertierung vom Typ des Ausdrucks in der `yield return`\-Anweisung in den generischen Typparameter erforderlich.  
  
 Sie können keine `yield return`\- oder `yield break`\-Anweisung in Methoden einbeziehen, die die folgenden Eigenschaften aufweisen:  
  
-   Anonyme Methoden.  Weitere Informationen finden Sie unter [Anonyme Methoden](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md).  
  
-   Methoden, die unsichere Blöcke enthalten.  Weitere Informationen finden Sie unter [Unsicher](../../../csharp/language-reference/keywords/unsafe.md).  
  
## Ausnahmebehandlung  
 Eine `yield return`\-Anweisung kann sich nicht in einem try\-catch\-Block befinden.  Eine `yield return`\-Anweisung kann sich im try\-Block einer try\-finally\-Anweisung befinden.  
  
 Eine `yield break`\-Anweisung kann sich in einem try\- oder catch\-Block befinden, nicht jedoch in einem finally\-Block.  
  
 Wenn der `foreach`\-Text \(außerhalb der Iteratormethode\) eine Ausnahme auslöst, wird ein `finally`\-Block in der Iteratormethode ausgeführt.  
  
## Technische Implementierung  
 Der folgende Code gibt einen `IEnumerable<string>` aus einer Iteratormethode zurück und durchläuft dann die Elemente.  
  
<CodeContentPlaceHolder>1</CodeContentPlaceHolder>  
 Der Aufruf von `MyIteratorMethod` führt nicht den Text der Methode aus.  Stattdessen gibt der Aufruf einen `IEnumerable<string>` in die Variable `elements` zurück.  
  
 Bei einer Iteration der `foreach`\-Schleife wird die Methode <xref:System.Collections.IEnumerator.MoveNext%2A> für `elements` aufgerufen.  Dieser Aufruf führt `MyIteratorMethod` aus, bis die nächste `yield return`\-Anweisung erreicht ist.  Der Ausdruck, der durch die `yield return`\-Anweisung zurückgegeben wird, ermittelt nicht nur den Wert der `element`\-Variable für die Verwendung im Schleifentext, sondern auch die <xref:System.Collections.Generic.IEnumerator%601.Current%2A>\-Eigenschaft der Elemente, die `IEnumerable<string>` ist.  
  
 Bei jeder nachfolgenden Iteration der `foreach`\-Schleife wird die Ausführung des Iteratortexts da fortgesetzt, wo sie beendet wurde, und endet dann wieder an einer `yield return`\-Anweisung.  Die `foreach`\-Schleife wird beendet, wenn das Ende der Iteratormethode oder eine `yield break`\-Anweisung erreicht wird.  
  
## Beispiel  
 Das folgende Beispiel weist eine `yield return`\-Anweisung auf, die sich innerhalb einer `for`\-Schleife befindet.  Jede Iteration des `foreach`\-Anweisungstexts in `Process` erzeugt einen Aufruf an die `Power`\-Iteratorfunktion.  Jeder Aufruf der Iteratorfunktion führt bei der nächsten Iteration der `for`\-Schleife zur nächsten Ausführung der `yield return`\-Anweisung.  
  
 Der Rückgabetyp der Iteratormethode ist <xref:System.Collections.IEnumerable>, was ein Iteratorschnittstellentyp ist.  Wird die Iteratormethode aufgerufen wird, gibt sie ein aufzählbares Objekt zurück, das die Potenzen einer Zahl enthält.  
  
 [!CODE [csrefKeywordsContextual#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#5)]  
  
## Beispiel  
 Das folgende Beispiel zeigt einen `get`\-Accessor, der ein Iterator ist.  Im Beispiel gibt jede `yield return`\-Anweisung eine Instanz einer benutzerdefinierten Klasse zurück.  
  
 [!CODE [csrefKeywordsContextual#21](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#21)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [foreach, in](../../../csharp/language-reference/keywords/foreach-in.md)   
 [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)