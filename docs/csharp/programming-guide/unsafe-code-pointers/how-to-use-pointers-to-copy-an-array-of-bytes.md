---
title: "Gewusst wie: Verwenden von Zeigern zum Kopieren eines Bytearrays (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "Arrays [C#], byte"
  - "Bytearrays [C#]"
  - "Zeiger [C#], Zum Kopieren von Bytes"
ms.assetid: ec16fbb4-a24e-45f5-a763-9499d3fabe0a
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden von Zeigern zum Kopieren eines Bytearrays (C#-Programmierhandbuch)
Im folgenden Beispiel werden Zeiger für das Kopieren von Bytes von einem Array in ein anderes verwendet.  
  
 In diesem Beispiel wird das [unsafe](../../../csharp/language-reference/keywords/unsafe.md)\-Schlüsselwort verwendet, das es Ihnen ermöglicht, in der `Copy`\-Methode Zeiger zu nutzen.  Die [fixed](../../../csharp/language-reference/keywords/fixed-statement.md)\-Anweisung wird zur Deklarierung von Zeigern auf das Quellarray und das Zielarray verwendet.  Dadurch wird die Position von Quell\- und Zielarray im Speicher *fixiert*, sodass diese von der Garbage Collection nicht verschoben werden.  Die Fixierung der Speicherblöcke für die Arrays wird aufgehoben, wenn der `fixed`\-Block abgeschlossen ist.  Da die `Copy`\-Methode in diesem Beispiel das `unsafe`\-Schlüsselwort verwendet, muss das Beispiel mit der **\/unsafe**\-Compileroption kompiliert werden.  Um in Visual Studio die Option festzulegen, klicken Sie mit der rechten Maustaste auf den Projektnamen, und klicken Sie dann auf **Eigenschaften**.  Wählen Sie auf der Registerkarte **Erstellen** die Option **Unsicheren Code zulassen** aus.  
  
## Beispiel  
 [!CODE [csProgGuidePointers#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#3)]  
  
 [!CODE [csProgGuidePointers#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#18)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Unsicherer Code und Zeiger](../../../csharp/programming-guide/unsafe-code-pointers/index.md)   
 [\/unsafe \(Enable Unsafe Mode\)](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md)   
 [Garbage Collection](../Topic/Garbage%20Collection.md)