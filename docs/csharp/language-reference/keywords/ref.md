---
title: "ref (C#-Referenz) | Microsoft Docs"
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
  - "ref_CSharpKeyword"
  - "ref"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Parameter [C#], ref"
  - "ref-Schlüsselwort [C#]"
ms.assetid: b8a5e59c-907d-4065-b41d-95bf4273c0bd
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# ref (C#-Referenz)
Das Schlüsselwort `ref` bewirkt, dass ein Argument durch einen Verweis, nicht durch einen Wert übergeben wird.  Durch das Übergeben durch einen Verweis wird jede Änderung am Parameter in der aufgerufenen Methode in der aufrufenden Methode wiedergegeben.  Wenn z. B. der Aufrufer einen lokalen Variablenausdruck oder einen Arrayelement\-Zugriffsausdruck übergibt und die aufgerufene Methode das Objekt ersetzt, auf das der Ref\-Parameter verweist, dann verweist die lokale Variable des Aufrufers oder das Arrayelement jetzt auf das neue Objekt.  
  
> [!NOTE]
>  Verwechseln Sie nicht das Konzept der Übergabe durch einen Verweis mit dem Konzept der Verweistypen.  Die beiden Konzepte sind nicht identisch.  Ein Methodenparameter kann durch `ref` geändert werden, unabhängig davon, ob es sich um einen Werttyp oder ein Verweistyp handelt.  Es gibt keine Boxing\-Konvertierung eines Werttyps, wenn er durch einen Verweis übergeben wird.  
  
 Um einen `ref`\-Parameter zu verwenden, müssen sowohl die Methodendefinition als auch die aufrufende Methode explizit das Schlüsselwort `ref` verwenden, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csrefKeywordsMethodParams#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#6)]  
  
 Ein Argument, das an einen `ref`\-Parameter übergeben wird, muss vor der Übergabe initialisiert werden.  Dies unterscheidet sich von den `out`\-Parametern, deren Argumente nicht explizit initialisiert werden müssen, bevor sie übergeben werden.  Weitere Informationen finden Sie unter [out](../../../csharp/language-reference/keywords/out.md).  
  
 Member einer Klasse können keine Signaturen haben, die sich nur durch `ref` und `out` voneinander unterscheiden.  Es tritt ein Compilerfehler auf, wenn der einzige Unterschied zwischen beiden Member eines Typs der ist, dass einer von ihnen über einen `ref`\-Parameter und der andere über einen `out`\-Parameter verfügt.  Der folgende Code wird z. B. nicht kompiliert.  
  
 [!CODE [csrefKeywordsMethodParams#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#2)]  
  
 Allerdings ist eine Überladung möglich, wenn eine Methode einen `ref`\- oder `out`\-Parameter hat und die andere über einen Werteparameter verfügt, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csrefKeywordsMethodParams#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#7)]  
  
 In anderen Situationen, die eine Signaturabstimmung benötigen, z. B. beim Ausblenden oder Überschreiben, sind `ref` und `out` Bestandteil der Signatur und passen nicht zueinander.  
  
 Eigenschaften sind keine Variablen.  Sie sind Methoden und können nicht an `ref`\-Parameter übergeben werden.  
  
 Weitere Informationen zum Übergeben von Arrays finden Sie unter [Übergeben von Arrays mithilfe von "ref" und "out"](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).  
  
 Sie können keines der beiden Schlüsselwörter `ref` und `out` für die folgenden Methodentypen verwenden:  
  
-   Async\-Methoden, die Sie mit dem [async](../../../csharp/language-reference/keywords/async.md)\-Modifizierer definieren.  
  
-   Iterator\-Methoden, die eine [yield return](../../../csharp/language-reference/keywords/yield.md)\- oder `yield break`\-Anweisung enthalten.  
  
## Beispiel  
 Die vorherigen Beispiele zeigen, was passiert, wenn Sie Werttypen durch einen Verweis übergeben.  Sie können auch das Schlüsselwort `ref` verwenden, um Verweistypen zu übergeben.  Die Übergabe eines Verweistyps durch einen Verweis ermöglicht es der aufgerufenen Methode, das Objekt in der aufrufenden Methode, auf die der Verweisparameter verweist, zu ersetzen.  Der Speicherort des Objekts wird als Wert des Verweisparameters an die Methode übergeben.  Wenn Sie den Wert am Speicherort des Parameters ändern \(um auf ein neues Objekt zu verweisen\), ändern Sie auch den Speicherort, auf den der Aufrufer verweist.  Im folgenden Beispiel wird eine Instanz eines Verweistyps als ein `ref`\-Parameter übergeben.  Weitere Informationen zum Übergeben von Verweistypen durch einen Wert und durch einen Verweis finden Sie unter [Übergeben von Verweistypparametern](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md).  
  
 [!CODE [csrefKeywordsMethodParams#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#8)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Übergeben von Parametern](../../../csharp/programming-guide/classes-and-structs/passing-parameters.md)   
 [Methodenparameter](../../../csharp/language-reference/keywords/method-parameters.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)