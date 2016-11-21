---
title: "&#220;bergeben von Arrays mithilfe von &quot;ref&quot; und &quot;out&quot; (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Arrays [C#], Übergeben mit ref und out"
ms.assetid: 6a2b261e-a1cc-49a6-b4f0-6cacae385a1e
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &#220;bergeben von Arrays mithilfe von &quot;ref&quot; und &quot;out&quot; (C#-Programmierhandbuch)
Wie alle [out](../../../csharp/language-reference/keywords/out.md)\-Parameter muss auch ein `out`\-Parameter eines Arraytyps vor der Verwendung zugewiesen werden, d. h., er muss vom Aufgerufenen zugewiesen werden.  Beispiel:  
  
 [!CODE [csProgGuideArrays#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#39)]  
  
 Wie alle [ref](../../../csharp/language-reference/keywords/ref.md)\-Parameter muss auch ein `ref`\-Parameter eines Arraytyps vom Aufrufer definitiv zugewiesen werden.  Daher besteht keine Notwendigkeit, dass die definitive Zuweisung vom Aufgerufenen vorgenommen wird.  Ein `ref`\-Parameter eines Arraytyps kann als Ergebnis des Aufrufs geändert werden.  Beispielsweise kann dem Array der Wert [NULL](../../../csharp/language-reference/keywords/null.md) zugewiesen werden, oder es kann mit einem anderen Array initialisiert werden.  Beispiel:  
  
 [!CODE [csProgGuideArrays#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#40)]  
  
 In den beiden folgenden Beispielen wird der Unterschied zwischen `out` und `ref` bei der Übergabe von Arrays an Methoden veranschaulicht.  
  
## Beispiel  
 In diesem Beispiel wird das Array `theArray` im Aufrufer \(der `Main`\-Methode\) deklariert und in der `FillArray`\-Methode initialisiert.  Anschließend werden die Elemente des Arrays an den Aufrufer zurückgegeben und angezeigt.  
  
 [!CODE [csProgGuideArrays#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#37)]  
  
## Beispiel  
 In diesem Beispiel wird das Array `theArray` im Aufrufer \(der `Main`\-Methode\) initialisiert und mithilfe des `ref`\-Parameters an die `FillArray`\-Methode übergeben.  Einige Arrayelemente werden in der `FillArray`\-Methode aktualisiert.  Anschließend werden die Elemente des Arrays an den Aufrufer zurückgegeben und angezeigt.  
  
 [!CODE [csProgGuideArrays#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#38)]  
  
## Siehe auch  
 [ref](../../../csharp/language-reference/keywords/ref.md)   
 [Modifizierer für out\-Parameter](../../../csharp/language-reference/keywords/out-parameter-modifier.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)