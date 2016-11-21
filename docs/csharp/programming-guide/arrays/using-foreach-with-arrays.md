---
title: "Verwenden von foreach mit Arrays (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], foreach"
  - "foreach-Anweisung [C#], Verwenden mit Arrays"
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Verwenden von foreach mit Arrays (C#-Programmierhandbuch)
C\# enthält außerdem die [foreach](../../../csharp/language-reference/keywords/foreach-in.md)\-Anweisung.  Diese Anweisung stellt eine einfache, klare Methode bereit, um die Elemente eines Arrays oder einer aufzählbaren Auflistung zu durchlaufen.  Die `foreach`\-Anweisung verarbeitet Elemente in der Reihenfolge, die vom Array oder Enumerator des Auflistungstyps zurückgegeben wird, also normalerweise vom nullten bis zum letzten Element.  Durch folgenden Code wird beispielsweise ein Array mit dem Namen `numbers` erstellt, das mithilfe der `foreach`\-Anweisung durchlaufen wird:  
  
 [!CODE [csProgGuideArrays#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#28)]  
  
 Bei mehrdimensionalen Arrays können Sie dieselbe Methode zum Durchlaufen der Elemente verwenden. Beispiel:  
  
 [!CODE [csProgGuideArrays#29](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#29)]  
  
 Bei mehrdimensionalen Arrays haben Sie jedoch eine größere Kontrolle über die Arrayelemente, indem Sie eine geschachtelte [for](../../../csharp/language-reference/keywords/for.md)\-Schleife verwenden.  
  
## Siehe auch  
 <xref:System.Array>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)