---
title: "Arrays als Objekte (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], Als Objekte"
ms.assetid: f76d4403-bd0a-42a0-9bc8-694c55b2c926
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Arrays als Objekte (C#-Programmierhandbuch)
In C\# sind Arrays tatsächlich Objekte und nicht nur adressierbare, zusammenhängende Speicherbereiche wie in C und C\+\+.  <xref:System.Array> ist der abstrakte Basistyp aller Bereichstypen.  Sie können die Eigenschaften sowie andere Klassenmember von <xref:System.Array> verwenden.  Ein Beispiel dafür wäre die Verwendung der <xref:System.Array.Length%2A>\-Eigenschaft, um die Länge eines Arrays abzurufen.  Mit folgendem Code wird die Länge des `numbers`\-Arrays, die `5` beträgt, einer Variablen mit dem Namen `lengthOfNumbers` zugewiesen:  
  
 [!CODE [csProgGuideArrays#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#3)]  
  
 Die <xref:System.Array>\-Klasse stellt viele andere nützliche Methoden und Eigenschaften bereit, z. B. zum Sortieren, Suchen und Kopieren von Arrays.  
  
## Beispiel  
 In diesem Beispiel wird mithilfe der <xref:System.Array.Rank%2A>\-Eigenschaft die Anzahl von Dimensionen eines Arrays angezeigt.  
  
 [!CODE [csProgGuideArrays#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#2)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)