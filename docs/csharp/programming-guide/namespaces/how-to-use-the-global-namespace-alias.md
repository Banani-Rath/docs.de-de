---
title: "Gewusst wie: Verwenden des globalen Namespacealias (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Aliase [C#]"
  - "Globaler Namespace [C#]"
  - "Namespaces [C#], Globaler Namespacequalifizierer"
ms.assetid: 98a1d89b-3c5a-44f7-8400-c4a3c0ec22a9
caps.latest.revision: 23
caps.handback.revision: 23
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden des globalen Namespacealias (C#-Programmierhandbuch)
Die Fähigkeit, auf einen Member im globalen [Namespace](../../../csharp/language-reference/keywords/namespace.md) zuzugreifen, ist nützlich, wenn der Member möglicherweise durch eine Entität gleichen Namens verdeckt ist.  
  
 Im folgenden Codebeispiel wird `Console` nach `TestApp.Console` aufgelöst, statt nach dem `Console`\-Typ im <xref:System>\-Namespace.  
  
 [!CODE [csProgGuide#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#1)]  
  
 [!CODE [csProgGuideNamespaces#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#1)]  
  
 Auch die Verwendung von `System.Console` führt zu einem Fehler, da der `System`\-Namespace von der `TestApp.System`\-Klasse verdeckt wird:  
  
 [!CODE [csProgGuideNamespaces#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#2)]  
  
 Sie können diesen Fehler jedoch umgehen, indem Sie `global::System.Console` folgendermaßen verwenden:  
  
 [!CODE [csProgGuideNamespaces#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#3)]  
  
 Wenn der linke Bezeichner `global` ist, beginnt die Suche nach dem rechten Bezeichner im globalen Namespace.  Die folgende Deklaration verweist beispielsweise auf `TestApp` als Member des globalen Namespaces.  
  
 [!CODE [csProgGuideNamespaces#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#4)]  
  
 Offensichtlich ist vom Erstellen eines eigenen Namespaces mit dem Namen `System` abzuraten, und Sie werden auch kaum jemals auf derartigen Code treffen.  In größeren Projekten ist es allerdings durchaus möglich, dass doppelte Namespaces auf die eine oder andere Weise vorkommen können.  In diesen Situationen garantiert der globale Namespacequalifizierer, dass Sie den Stammnamespace angeben können.  
  
## Beispiel  
 In diesem Beispiel schließt der `System`\-Namespace die `TestClass`\-Klasse ein, sodass `global::System.Console` benötigt wird, um auf die `System.Console`\-Klasse zu verweisen, die durch den `System`\-Namespace verdeckt wird.  Außerdem wird mit dem Alias `colAlias` auf den `System.Collections`\-Namespace verwiesen. Deshalb wurde die Instanz von <xref:System.Collections.Hashtable?displayProperty=fullName> mit diesem Alias statt mit dem Namespace erstellt.  
  
 [!CODE [csProgGuideNamespaces#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#5)]  
  
  **A 1**  
**B 2**  
**C 3**   
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Namespaces](../../../csharp/programming-guide/namespaces/index.md)   
 [. Operator](../../../csharp/language-reference/operators/member-access-operator.md)   
 [Operator ::](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)   
 [extern](../../../csharp/language-reference/keywords/extern.md)