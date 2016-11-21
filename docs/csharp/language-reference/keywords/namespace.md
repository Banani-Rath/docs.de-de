---
title: "Namespace (C#-Referenz) | Microsoft Docs"
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
  - "namespace_CSharpKeyword"
  - "namespace"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Namespaceschlüsselwort [C#]"
  - "Gültigkeitsbereich [C#]"
ms.assetid: 0a788423-9110-42e0-97d9-bda41ca4870f
caps.latest.revision: 28
caps.handback.revision: 28
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Namespace (C#-Referenz)
Das `namespace`\-Schlüsselwort wird verwendet, um einen Bereich zu deklarieren, der einen Satz von verknüpfte Objekte enthält.  Sie können einen Namespace verwenden, um Codeelemente zu organisieren und \- global eindeutige Typen zu erstellen.  
  
 [!CODE [csrefKeywordsNamespace#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#1)]  
  
## Hinweise  
 in einem Namespace mindestens eine Deklaration eines der folgenden Typen:  
  
-   ein weiterer Namespace  
  
-   [\-Klasse](../../../csharp/language-reference/keywords/class.md)  
  
-   [interface](../../../csharp/language-reference/keywords/interface.md)  
  
-   [struct](../../../csharp/language-reference/keywords/struct.md)  
  
-   [enum](../../../csharp/language-reference/keywords/enum.md)  
  
-   [Delegat](../../../csharp/language-reference/keywords/delegate.md)  
  
 Unabhängig davon, ob Sie einen Namespace in einer C\#\-Quelldatei explizit deklarieren, fügt der Compiler einen Standardnamespace hinzu.  Dieser unbenannte Namespace, der manchmal auch als globaler Namespace bezeichnet wird, ist in jeder Datei vorhanden.  Jeder Bezeichner im globalen Namespace kann in einem benannten Namespace eingesetzt werden.  
  
 Implizit verfügen Namespaces über öffentlichen Zugriff. Dies kann nicht geändert werden.  Einen Diskurs über Zugriffsmodifizierer in Namespaces, die Elementen zugewiesen werden können, finden Sie unter [Zugriffsmodifizierer](../../../csharp/language-reference/keywords/access-modifiers.md).  
  
 Ein Namespace kann in zwei oder mehr Deklarationen definiert werden.  Im folgenden Beispiel werden zwei Klassen als Teil des `MyCompany`\-Namespaces definiert:  
  
 [!CODE [csrefKeywordsNamespace#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#2)]  
  
## Beispiel  
 Im folgenden Beispiel wird gezeigt, wie eine statische Methode in einem geschachtelten Namespace aufgerufen wird.  
  
 [!CODE [csrefKeywordsNamespace#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#3)]  
  
## Weitere Informationen  
 Weitere Informationen zur Verwendung von Namespaces finden Sie in den folgenden Themen:  
  
-   [Namespaces](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [Verwenden von Namespaces](../../../csharp/programming-guide/namespaces/using-namespaces.md)  
  
-   [Gewusst wie: Verwenden des globalen Namespacealias](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Namespaceschlüsselwörter](../../../csharp/language-reference/keywords/namespace-keywords.md)   
 [Verwenden](../../../csharp/language-reference/keywords/using.md)