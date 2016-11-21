---
title: "Generische Delegaten (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Delegaten [C#], Generisch"
  - "Generika [C#], Delegaten"
ms.assetid: bdea509c-44c1-4309-aaa9-15c7aee009df
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Generische Delegaten (C#-Programmierhandbuch)
Ein [Delegat](../../../csharp/language-reference/keywords/delegate.md) kann seine eigenen Typparameter definieren.  Wie im folgenden Beispiel gezeigt, kann Code, der auf den generischen Delegaten verweist, das Typargument zum Erstellen eines geschlossenen konstruierten Typs angeben, genau wie wenn eine generische Klasse instanziiert oder eine generische Methode aufgerufen wird:  
  
 [!CODE [csProgGuideGenerics#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#36)]  
  
 C\# 2.0 verfügt über ein neues Feature. Dieses Feature wird als Methodengruppenkonvertierung bezeichnet und gilt sowohl für konkrete als auch für generische Delegattypen. Damit können Sie die vorhergehende Zeile mit folgender vereinfachter Syntax schreiben:  
  
 [!CODE [csProgGuideGenerics#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#37)]  
  
 Delegaten, die innerhalb einer generischen Klasse definiert sind, können die Typparameter der generischen Klasse auf die gleiche Art und Weise verwenden wie Klassenmethoden diese verwenden.  
  
 [!CODE [csProgGuideGenerics#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#38)]  
  
 Code, der auf den Delegaten verweist, muss das Typargument der enthaltenden Klasse wie folgt angeben:  
  
 [!CODE [csProgGuideGenerics#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#39)]  
  
 Generische Delegaten sind besonders nützlich zum Definieren von Ereignissen, die auf dem typischen Entwurfsmuster basieren, denn das Absenderargument kann mit starker Typisierung versehen werden und muss nicht länger in das bzw. aus dem <xref:System.Object> umgewandelt werden.  
  
 [!CODE [csProgGuideGenerics#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#40)]  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Einführung in Generika](../../../csharp/programming-guide/generics/introduction-to-generics.md)   
 [Generische Methoden](../../../csharp/programming-guide/generics/generic-methods.md)   
 [Generische Klassen](../../../csharp/programming-guide/generics/generic-classes.md)   
 [Generische Schnittstellen](../../../csharp/programming-guide/generics/generic-interfaces.md)   
 [Delegaten](../../../csharp/programming-guide/delegates/index.md)   
 [Generika](../Topic/Generics%20in%20the%20.NET%20Framework.md)