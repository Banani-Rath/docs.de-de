---
title: "&#220;bergeben von Parametern (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Argumente [C#]"
  - "C#-Sprache, Methodenparameter"
  - "Methoden [C#], Übergeben von Parametern"
  - "Parameter [C#], Übergeben"
  - "Übergeben von Parametern (C#)"
ms.assetid: a5c3003f-7441-4710-b8b1-c79de77e0b77
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &#220;bergeben von Parametern (C#-Programmierhandbuch)
In C\# können Argumente als Wert oder als Verweis an Parameter übergeben werden.  Durch Übergeben als Verweis können Funktionsmember, Methoden, Eigenschaften, Indexer, Operatoren und Konstruktoren den Wert der Parameter ändern, und diese Änderung bleibt in der Aufrufumgebung erhalten.  Um einen Parameter als Verweis zu übergeben, verwenden Sie das `ref`\-Schlüsselwort oder das `out`\-Schlüsselwort.  Zur besseren Übersicht wird in den Beispielen dieses Themas nur das `ref`\-Schlüsselwort verwendet.  Weitere Informationen zum Unterschied zwischen `ref` und `out` erhalten Sie unter [ref](../../../csharp/language-reference/keywords/ref.md), [out](../../../csharp/language-reference/keywords/out.md) und [Übergeben von Arrays mithilfe von "ref" und "out"](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).  
  
 Im folgenden Beispiel werden die Unterschiede zwischen Wert\- und Verweisparametern veranschaulicht.  
  
 [!CODE [csProgGuideParameters#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#10)]  
  
 Weitere Informationen finden Sie unter den folgenden Themen:  
  
-   [Übergeben von Werttypparametern](../../../csharp/programming-guide/classes-and-structs/passing-value-type-parameters.md)  
  
-   [Übergeben von Verweistypparametern](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md)  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Methoden](../../../csharp/programming-guide/classes-and-structs/methods.md)