---
title: "Schnittstelleneigenschaften (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Schnittstellen [C#], Eigenschaften"
  - "Eigenschaften [C#], Auf Schnittstellen"
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Schnittstelleneigenschaften (C#-Programmierhandbuch)
Eigenschaften können für [Schnittstelle](../../../csharp/language-reference/keywords/interface.md) deklariert werden.  Das folgende Beispiel zeigt einen Accessor für einen Schnittstellenindexer:  
  
 [!CODE [csProgGuideProperties#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#14)]  
  
 Der Accessor einer Schnittstelleneigenschaft enthält keinen Text.  Ein Accessor wird also verwendet, um anzugeben, ob die Eigenschaft Lese\- und Schreibzugriffe gleichzeitig bzw. jeweils nur Schreib\- oder Lesezugriffe unterstützt.  
  
## Beispiel  
 In diesem Beispiel hat die `IEmployee`\-Schnittstelle eine Lesen\-\/Schreiben\-Eigenschaft `Name` und eine Nur\-Schreiben\-Eigenschaft `Counter`.  Die `Employee`\-Klasse implementiert die `IEmployee`\-Schnittstelle und verwendet diese beiden Eigenschaften.  Der Name eines neuen Mitarbeiters und die aktuelle Anzahl der Mitarbeiter werden vom Programm gelesen, und der Mitarbeitername sowie die berechnete Anzahl von Mitarbeitern wird angezeigt.  
  
 Sie könnten den vollqualifizierten Namen der Eigenschaft verwenden, die auf die Schnittstelle verweist, in der der Member deklariert ist.  Beispiele:  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 Dies wird als [Explizite Schnittstellenimplementierung](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md) bezeichnet.  Wenn beispielsweise zwei Schnittstellen, `ICitizen` und `IEmployee`, von der `Employee`\-Klasse implementiert sind und beide Schnittstellen über die `Name`\-Eigenschaft verfügen, muss der Schnittstellenmember explizit implementiert werden.  Mit der folgenden Eigenschaftendeklaration  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 wird die `Name`\-Eigenschaft für die `IEmployee`\-Schnittstelle implementiert, während mit der Deklaration  
  
 [!CODE [csProgGuideProperties#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#17)]  
  
 die `Name`\-Eigenschaft für die `ICitizen`\-Schnittstelle implementiert wird.  
  
 [!CODE [csProgGuideProperties#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#15)]  
  
  **`210 Hazem Abolrous`**    
## Beispielausgabe  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Eigenschaften](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Verwenden von Eigenschaften](../../../csharp/programming-guide/classes-and-structs/using-properties.md)   
 [Vergleich zwischen Eigenschaften und Indexern](../../../csharp/programming-guide/indexers/comparison-between-properties-and-indexers.md)   
 [Indexer](../../../csharp/programming-guide/indexers/index.md)   
 [Schnittstellen](../../../csharp/programming-guide/interfaces/index.md)