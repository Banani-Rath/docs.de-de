---
title: "Operator -&gt; (C#-Referenz) | Microsoft Docs"
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
  - "->_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "->-Operator [C#]"
  - "Memberzugriffsoperator (->) [C#]"
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Operator -&gt; (C#-Referenz)
Der Operator `->` kombiniert Zeigerdereferenzierung und Memberzugriff.  
  
## Hinweise  
 Ein Ausdruck der Form  
  
```  
x->y  
```  
  
 \(wobei `x` ein Zeiger vom Typ `T*` und `y` ein Member von `T` ist\) ist äquivalent zu  
  
```  
(*x).y  
```  
  
 Der `->`\-Operator kann nur in Code verwendet werden, der als [unsicher](../../../csharp/language-reference/keywords/unsafe.md) markiert ist.  
  
 Der Operator `->` kann nicht überladen werden.  
  
## Beispiel  
 [!CODE [csRefOperators#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#15)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)