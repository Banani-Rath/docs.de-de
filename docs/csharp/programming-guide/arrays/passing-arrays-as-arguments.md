---
title: "&#220;bergeben von Arrays als Argumente (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], Übergeben als Argumente"
ms.assetid: f3a0971e-c87c-4a1f-8262-bc0a3b712772
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &#220;bergeben von Arrays als Argumente (C#-Programmierhandbuch)
Arrays können als Argumente an Methodenparameter übergeben werden.  Da Arrays Verweistypen sind, kann die Methode den Wert der Elemente ändern.  
  
## Übergeben von eindimensionalen Arrays als Argumente  
 Sie können ein initialisiertes eindimensionales Array an eine Methode übergeben.  Die folgende Anweisung sendet z. B. ein Array an eine print\-Methode.  
  
 [!CODE [csProgGuideArrays#34](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#34)]  
  
 Der folgende Code zeigt eine Teilimplementierung der print\-Methode.  
  
 [!CODE [csProgGuideArrays#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#33)]  
  
 Sie können ein neues Array in einem Schritt initialisieren und übergeben, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [CsProgGuideArrays#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#35)]  
  
## Beispiel  
  
### Beschreibung  
 Im folgenden Beispiel wird ein Zeichenfolgenarray initialisiert und als Argument an eine `PrintArray`\-Methode für Zeichenfolgen übergeben.  Die Methode zeigt die Elemente des Arrays an.  Anschließend werden die Methoden `ChangeArray` und `ChangeArrayElement` aufgerufen, um zu veranschaulichen, dass das Senden eines Arrayarguments nach Wert Änderungen an den Arrayelementen nicht verhindert.  
  
### Code  
 [!CODE [csProgGuideArrays#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#30)]  
  
## Übergeben von mehrdimensionalen Arrays als Argumente  
 Die Übergabe eines initialisierten mehrdimensionalen Arrays an eine Methode erfolgt wie bei einem eindimensionalen Array.  
  
 [!CODE [csProgGuideArrays#41](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#41)]  
  
 Der folgende Code zeigt die Teildeklaration einer print\-Methode, die ein zweidimensionales Array als Argument erfordert.  
  
 [!CODE [csProgGuideArrays#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#36)]  
  
 Sie können ein neues Array in einem Schritt initialisieren und übergeben, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideArrays#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#32)]  
  
## Beispiel  
  
### Beschreibung  
 Im folgenden Beispiel wird ein zweidimensionales Array mit ganzen Zahlen initialisiert und an die `Print2DArray`\-Methode übergeben.  Die Methode zeigt die Elemente des Arrays an.  
  
### Code  
 [!CODE [csProgGuideArrays#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#31)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Mehrdimensionale Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)