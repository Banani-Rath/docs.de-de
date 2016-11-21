---
title: "fixed-Anweisung (C#-Referenz) | Microsoft Docs"
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
  - "fixed_CSharpKeyword"
  - "fixed"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "fixed-Schlüsselwort [C#]"
ms.assetid: 7ea6db08-ad49-4a7a-b934-d8c4acad1c3a
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# fixed-Anweisung (C#-Referenz)
Die `fixed`\-Anweisung verhindert, dass der Garbage Collector eine bewegliche Variable verschiebt.  Die `fixed`\-Anweisung ist nur in einem [unsicheren](../../../csharp/language-reference/keywords/unsafe.md) Kontext erlaubt.  `Fixed` kann auch verwendet werden, um [Puffer mit fester Größe](../../../csharp/programming-guide/unsafe-code-pointers/fixed-size-buffers.md) zu erstellen.  
  
 Die `fixed`\-Anweisung legt einen Zeiger auf eine verwaltete Variable fest und "fixiert" diese Variable während der Ausführung der Anweisung.  Zeiger auf bewegliche, verwaltete Variablen wären ohne `fixed` von geringem Nutzen, da Garbage Collection die Variablen auf unvorhersehbare Weise verschieben könnte.  Der C\#\-Compiler erlaubt die Zuweisung von Zeigern auf verwaltete Variablen nur in einer `fixed`\-Anweisung.  
  
 [!CODE [csrefKeywordsFixedLock#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#1)]  
  
 Sie können einen Zeiger initialisieren, indem Sie ein Array, eine Zeichenfolge, einen Puffer mit fester Größe oder die Adresse einer Variablen verwenden.  Das folgende Beispiel veranschaulicht die Verwendung von variablen Adressen, Arrays und Zeichenfolgen.  Weitere Informationen über Puffer mit fester Größe finden Sie unter [Puffer fester Größe](../../../csharp/programming-guide/unsafe-code-pointers/fixed-size-buffers.md).  
  
 [!CODE [csrefKeywordsFixedLock#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#2)]  
  
 Mehrere Zeiger können initialisiert werden, solange sie denselben Typ aufweisen.  
  
```  
fixed (byte* ps = srcarray, pd = dstarray) {...}  
```  
  
 Um Zeiger verschiedener Typen zu initialisieren, verschachteln Sie einfach `fixed`\-Anweisungen, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csrefKeywordsFixedLock#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#3)]  
  
 Nach der Ausführung des Anweisungscodes können beliebige fixierte Variablen wieder gelöst und für Garbage Collection freigegeben werden.  Zeigen Sie daher nicht außerhalb der `fixed`\-Anweisung auf solche Variablen.  
  
> [!NOTE]
>  Zeiger, die in **fixed**\-Anweisungen initialisiert wurden, können nicht geändert werden.  
  
 Im nicht sicheren Modus kann Speicher auf dem Stapel belegt werden. Dort unterliegt er nicht Garbage Collection und muss daher nicht fixiert werden.  Weitere Informationen finden Sie unter [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md).  
  
## Beispiel  
 [!CODE [csrefKeywordsFixedLock#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsFixedLock#4)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Unsicher](../../../csharp/language-reference/keywords/unsafe.md)   
 [Puffer fester Größe](../../../csharp/programming-guide/unsafe-code-pointers/fixed-size-buffers.md)