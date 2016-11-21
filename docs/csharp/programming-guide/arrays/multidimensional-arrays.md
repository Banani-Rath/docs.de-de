---
title: "Mehrdimensionale Arrays (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Arrays [C#], Mehrdimensional"
  - "Mehrdimensionale Arrays [C#]"
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Mehrdimensionale Arrays (C#-Programmierhandbuch)
Arrays können über mehr als eine Dimension verfügen.  Durch die folgende Deklaration wird z. B. ein zweidimensionales Array mit vier Zeilen und zwei Spalten erstellt.  
  
 [!CODE [csProgGuideArrays#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#11)]  
  
 Durch die nachstehende Deklaration wird ein Array mit den drei Dimensionen 4, 2 und 3 erstellt.  
  
 [!CODE [csProgGuideArrays#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#12)]  
  
## Arrayinitialisierung  
 Sie können das Array, wie im folgenden Beispiel dargestellt, während der Deklaration initialisieren.  
  
 [!CODE [csProgGuideArrays#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#13)]  
  
 Das Array kann auch ohne Angabe des Rangs initialisiert werden.  
  
 [!CODE [csProgGuideArrays#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#14)]  
  
 Falls Sie eine Arrayvariable ohne Initialisierung deklarieren möchten, müssen Sie der Variablen mit dem Operator `new` ein Array zuweisen.  Im folgenden Beispiel ist die Verwendung von `new` dargestellt:  
  
 [!CODE [csProgGuideArrays#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#15)]  
  
 Im folgenden Beispiel wird ein Wert einem bestimmten Arrayelement zugeordnet.  
  
 [!CODE [csProgGuideArrays#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#16)]  
  
 Entsprechend ruft das folgende Beispiel den Wert eines bestimmten Arrayelements ab und weist es variablem `elementValue` zu.  
  
 [!CODE [csProgGuideArrays#42](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#42)]  
  
 Das folgende Codebeispiel initialisiert die Arrayelemente auf die Standardwerte \(gilt nicht für verzweigte Arrays\).  
  
 [!CODE [csProgGuideArrays#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#17)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Arrays](../../../csharp/programming-guide/arrays/index.md)   
 [Eindimensionale Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [Verzweigte Arrays](../../../csharp/programming-guide/arrays/jagged-arrays.md)