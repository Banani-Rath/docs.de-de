---
title: "Generische Typparameter (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Generika [C#], Typparameter"
  - "Typparameter [C#]"
ms.assetid: a03b0ab2-0606-4b41-b7bf-e64d5bb4d18f
caps.latest.revision: 23
caps.handback.revision: 23
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Generische Typparameter (C#-Programmierhandbuch)
Bei der Definition eines generischen Typs oder einer Methode ist ein Typparameter ein Platzhalter für einen bestimmten Typ, den ein Client angibt, wenn eine Variable des generischen Typs instanziiert werden soll.  Eine generische Klasse, z. B. die unter [Einführung in Generika](../../../csharp/programming-guide/generics/introduction-to-generics.md) aufgelistete Klasse `GenericList<T>`, kann nicht ohne Anpassung verwendet werden, denn die Klasse ist nicht wirklich ein Typ. Sie ist mehr wie eine Kopie eines Typs.  Um `GenericList<T>` verwenden zu können, muss der Clientcode einen konstruierten Typ deklarieren und instanziieren, indem er ein Typargument in spitzen Klammern angibt.  Das Typargument für diese spezielle Klasse kann jeder Typ sein, der vom Compiler erkannt wird.  Instanzen von konstruierten Typen können in beliebiger Zahl erstellt werden, wobei jede Instanz ein anderes Typargument verwendet, z. B.:  
  
 [!CODE [csProgGuideGenerics#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#7)]  
  
 Bei jeder dieser Instanzen von `GenericList<T>` wird jedes Vorkommen von `T` in der Klasse zur Laufzeit durch das Typargument ersetzt.  Aufgrund dieser Ersetzung werden drei separate typsichere und effiziente Objekte mithilfe einer einzigen Klassendefinition erstellt.  Weitere Informationen dazu, wie diese Ersetzung von der CLR ausgeführt wird, finden Sie unter [Generika zur Laufzeit](../../../csharp/programming-guide/generics/generics-in-the-run-time.md).  
  
## Richtlinien für die Benennung von Typparametern  
  
-   **Verwenden** Sie zur Benennung von generischen Typparametern beschreibende Namen, es sei denn, ein Name aus einem einzelnen Buchstaben reicht als Erklärung völlig aus, und ein beschreibender Name würde das Verständnis für den Namen nicht wirklich erhöhen.  
  
     [!CODE [csProgGuideGenerics#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#8)]  
  
-   **Verwenden** Sie T als Typparametername für Typen, die einen einzelnen Buchstaben als Typparameter haben.  
  
     [!CODE [csProgGuideGenerics#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#9)]  
  
-   **Verwenden** Sie das Präfix "T" für beschreibende Typparameternamen.  
  
     [!CODE [csProgGuideGenerics#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#10)]  
  
-   **Überlegen** Sie, ob Sie Einschränkungen, die für einen Typparameter gelten, im Namen des Parameters angeben möchten.  Ein auf `ISession` eingeschränkter Parameter könnte z. B. `TSession` genannt werden.  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Generika](../../../csharp/programming-guide/generics/index.md)   
 [Unterschiede zwischen C\+\+\-Vorlagen und C\#\-Generika](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)