---
title: "Eindimensionale Arrays (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], Eindimensional"
  - "Eindimensionale Arrays [C#]"
ms.assetid: 2cec1196-1de0-49d2-baf2-c607c33310e8
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Eindimensionale Arrays (C#-Programmierhandbuch)
Sie können ein eindimensionales Array mit fünf ganzen Zahlen deklarieren, wie im folgenden Beispiel gezeigt:  
  
 [!CODE [csProgGuideArrays#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#4)]  
  
 Dieses Array umfasst Elemente von `array[0]` bis `array[4]`.  Der Operator [new](../../../csharp/language-reference/keywords/new.md) wird zum Erstellen des Arrays und zum Initialisieren der Arrayelemente mit ihren Standardwerten verwendet.  In diesem Beispiel werden alle Arrayelemente mit Null initialisiert.  
  
 Arrays, in denen Zeichenfolgenelemente gespeichert werden, können auf dieselbe Weise deklariert werden.  Beispiele:  
  
 [!CODE [csProgGuideArrays#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#5)]  
  
## Arrayinitialisierung  
 Ein Array kann bei der Deklaration initialisiert werden. In diesem Fall ist kein Rangspezifizierer erforderlich, da er bereits durch die Anzahl der Elemente in der Initialisierungsliste angegeben wird.  Beispiele:  
  
 [!CODE [csProgGuideArrays#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#6)]  
  
 Ein Zeichenfolgenarray kann auf dieselbe Weise initialisiert werden.  Im Folgenden sehen Sie die Deklaration eines Zeichenfolgenarrays, in dem jedes Arrayelement durch den Namen eines Wochentages initialisiert wird:  
  
 [!CODE [csProgGuideArrays#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#7)]  
  
 Bei der Initialisierung eines Arrays während der Deklaration können Sie die Eingabe folgendermaßen verkürzen:  
  
 [!CODE [csProgGuideArrays#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#8)]  
  
 Eine Arrayvariable kann auch ohne Initialisierung deklariert werden. Sie müssen jedoch den Operator `new` verwenden, wenn Sie dieser Variablen ein Array zuweisen.  Beispiele:  
  
 [!CODE [csProgGuideArrays#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#9)]  
  
 In C\# 3.0 werden implizit typisierte Arrays eingeführt.  Weitere Informationen finden Sie unter [Implizit typisierte Arrays](../../../csharp/programming-guide/arrays/implicitly-typed-arrays.md).  
  
## Werttyp\- und Referenztyparrays  
 Betrachten Sie die folgende Arraydeklaration:  
  
 [!CODE [csProgGuideArrays#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#10)]  
  
 Das Ergebnis dieser Anweisung hängt davon ab, ob `SomeType` ein Werttyp oder ein Referenztyp ist.  Wenn dies ein Werttyp ist, wird durch die Anweisung ein Array mit 10 Elementen jeweils mit dem Typ `SomeType` erstellt.  Wenn `SomeType` ein Referenztyp ist, wird durch die Anweisung ein Array mit 10 Elementen erstellt, von denen jedes mit einem Nullverweis initialisiert wird.  
  
 Weitere Informationen zu Wert\- und Referenztypen finden Sie unter [Typen](../../../csharp/language-reference/keywords/types.md).  
  
## Siehe auch  
 <xref:System.Array>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)