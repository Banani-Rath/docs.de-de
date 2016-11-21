---
title: "&lt;remarks&gt; (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "remarks"
  - "<remarks>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<remarks> (C#-XML-Tag)"
  - "remarks (C#-XML-Tag)"
ms.assetid: f8641391-31f3-4735-af7a-c502a5b6a251
caps.latest.revision: 15
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &lt;remarks&gt; (C#-Programmierhandbuch)
## Syntax  
  
```  
<remarks>description</remarks>  
```  
  
#### Parameter  
 `Description`  
 eine Beschreibung des Members.  
  
## Hinweise  
 Mittels des \<remarks\>\-Tags werden Informationen über einen Typ hinzugefügt. Diese dienen als Ergänzung zu den mit [\<summary\>](../../../csharp/programming-guide/xmldoc/summary.md) angegebenen Informationen.  Diese Informationen werden im [Object Browser Window](http://msdn.microsoft.com/de-de/3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda) angezeigt.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit ["\/doc"](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#9)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Empfohlene Tags für Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)