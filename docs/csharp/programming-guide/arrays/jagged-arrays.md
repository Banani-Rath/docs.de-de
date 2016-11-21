---
title: "Verzweigte Arrays (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], Verzweigt"
  - "Verzweigte Arrays [C#]"
ms.assetid: 537c65a6-0e0a-4a00-a2b8-086f38519c70
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Verzweigte Arrays (C#-Programmierhandbuch)
Ein verzweigtes Array ist ein Array, dessen Elemente wiederum Arrays sind.  Die Elemente eines verzweigten Arrays können über unterschiedliche Dimensionen und Größen verfügen.  Ein verzweigtes Array wird manchmal auch als "Array von Arrays" bezeichnet. Die folgenden Beispiele zeigen, wie verzweigte Arrays deklariert und initialisiert werden und wie auf sie zugegriffen wird.  
  
 Im Folgenden sehen Sie die Deklaration eines eindimensionalen Arrays mit drei Elementen, von denen jedes ein eindimensionales Array von ganzen Zahlen darstellt:  
  
 [!CODE [csProgGuideArrays#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#19)]  
  
 Bevor Sie `jaggedArray` verwenden können, müssen die Elemente des Arrays initialisiert werden.  Sie können die Elemente wie folgt initialisieren:  
  
 [!CODE [csProgGuideArrays#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#20)]  
  
 Jedes Element ist ein eindimensionales Array von ganzen Zahlen.  Alle Elemente sind Arrays. Das erste verfügt über 5, das zweite über 4 und das dritte über 2 ganze Zahlen.  
  
 Es besteht auch die Möglichkeit, Initialisierungen zu verwenden, um die Arrayelemente mit Werten aufzufüllen. In diesem Fall ist die Arraygröße nicht erforderlich.  Beispiele:  
  
 [!CODE [csProgGuideArrays#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#21)]  
  
 Das Array kann auch, wie im Folgenden dargestellt, während der Deklaration initialisiert werden:  
  
 [!CODE [csProgGuideArrays#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#22)]  
  
 Sie können die folgende Kurzform verwenden.  Beachten Sie, dass Sie den Operator `new` bei der Initialisierung der Elemente nicht weglassen können, weil es für die Elemente keine Standardinitialisierung gibt:  
  
 [!CODE [csProgGuideArrays#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#23)]  
  
 Ein verzweigtes Array ist ein Array von Arrays, und deshalb sind seine Elemente Verweistypen und werden mit `null` initialisiert.  
  
 In den folgenden Beispielen wird veranschaulicht, wie der Zugriff auf einzelne Arrayelemente erfolgt:  
  
 [!CODE [csProgGuideArrays#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#24)]  
  
 Verzweigte und mehrdimensionale Arrays können auch kombiniert werden.  Im Folgenden sehen Sie die Beschreibung und Initialisierung eines eindimensionalen verzweigten Arrays, das drei zweidimensionale Arrayelemente unterschiedlicher Größe enthält.  Weitere Informationen zu zweidimensionalen Arrays finden Sie unter [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md).  
  
 [!CODE [csProgGuideArrays#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#25)]  
  
 Im folgenden Beispiel wird dargestellt, wie Sie auf einzelne Elemente zugreifen können. Der Wert von Element `[1,0]` des ersten Arrays wird angezeigt \(Wert `5`\):  
  
 [!CODE [csProgGuideArrays#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#26)]  
  
 Die Methode `Length` gibt die Anzahl der Arrays zurück, die im verzweigten Array enthalten sind.  Angenommen, Sie hätten das vorherige Array deklariert, dann gibt die Zeile:  
  
 [!CODE [csProgGuideArrays#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#27)]  
  
 Gibt einen Wert von 3 zurück.  
  
## Beispiel  
 In diesem Beispiel wird ein Array erstellt, dessen Elemente selbst Arrays sind.  Jedes Arrayelement hat eine andere Größe.  
  
 [!CODE [csProgGuideArrays#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#18)]  
  
## Siehe auch  
 <xref:System.Array>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)