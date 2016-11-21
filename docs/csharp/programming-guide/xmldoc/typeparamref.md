---
title: "&lt;typeparamref&gt; (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "typeparamref"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<typeparamref> (C#-XML-Tag)"
  - "typeparamref (C#-XML-Tag)"
ms.assetid: 6d8ffc58-12c5-4688-8db6-833a7ded5886
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &lt;typeparamref&gt; (C#-Programmierhandbuch)
## Syntax  
  
```  
<typeparamref name="name"/>  
```  
  
#### Parameter  
 `name`  
 Der Name des Typparameters.  Der Name muss in doppelte Anführungszeichen \(**" "**\) eingeschlossen werden.  
  
## Hinweise  
 Weitere Informationen zu Typparametern in generischen Typen und Methoden finden Sie unter [Generika](../../../csharp/programming-guide/generics/index.md).  
  
 Verwenden Sie dieses Tag, damit Consumer der Dokumentationsdatei das Wort auf ganz bestimmte Art formatieren können, zum Beispiel kursiv.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit ["\/doc"](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#13)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Empfohlene Tags für Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)