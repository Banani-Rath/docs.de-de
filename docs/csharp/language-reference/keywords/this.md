---
title: "this (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "this"
  - "this_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "this-Schlüsselwort [C#]"
ms.assetid: d4f827fe-4710-410b-89b8-867dad44b8a3
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# this (C#-Referenz)
Das `this`\-Schlüsselwort verweist auf die aktuelle Instanz der Klasse und wird auch als Modifizierer des ersten Parameters einer Erweiterungsmethode verwendet.  
  
> [!NOTE]
>  In diesem Artikel wird die Verwendung von `this` mit Klasseninstanzen erläutert.  Weitere Informationen über die Verwendung in Erweiterungsmethoden finden Sie unter [Erweiterungsmethoden](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).  
  
 Im Folgenden sind häufige Verwendungen von `this` aufgeführt:  
  
-   Kennzeichnen von Membern, die durch ähnliche Namen ausgeblendet sind, z. B.:  
  
 [!CODE [csrefKeywordsAccess#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#4)]  
  
-   Übergeben eines Objekts als Parameter an andere Methoden, z. B.:  
  
    ```  
    CalcTax(this);  
    ```  
  
-   Deklarieren von Indexern, z. B.:  
  
 [!CODE [csrefKeywordsAccess#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#5)]  
  
 Da statische Memberfunktionen auf der Klassenebene bestehen und nicht Teil eines Objekts sind, besitzen sie keinen `this`\-Zeiger.  Es ist nicht zulässig, in einer statischen Methode auf `this` zu verweisen.  
  
## Beispiel  
 In diesem Beispiel wird `this` zum Kennzeichnen der `Employee`\-Klassenmember `name` und `alias` verwendet, die durch ähnliche Namen ausgeblendet sind.  Es wird ebenfalls eingesetzt, um ein Objekt an die `CalcTax`\-Methode, die einer anderen Klasse angehört, zu übergeben.  
  
 [!CODE [csrefKeywordsAccess#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#3)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Basis](../../../csharp/language-reference/keywords/base.md)   
 [Methoden](../../../csharp/programming-guide/classes-and-structs/methods.md)