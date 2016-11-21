---
title: "&lt;paramref&gt; (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "paramref"
  - "<paramref>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<paramref> (C#-XML-Tag)"
  - "paramref (C#-XML-Tag)"
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &lt;paramref&gt; (C#-Programmierhandbuch)
## Syntax  
  
```  
<paramref name="name"/>  
```  
  
#### Parameter  
 `name`  
 der Name des Parameters, auf den verwiesen werden soll.  Der Name muss in doppelte Anführungszeichen \(**" "**\) eingeschlossen werden.  
  
## Hinweise  
 Das \<paramref\>\-Tag stellt eine Möglichkeit dar, anzuzeigen, dass es sich bei einem Wort im Codekommentar, beispielsweise in einem \<summary\>\- oder \<remarks\>\-Block, um einen Parameter handelt.  Die XML\-Datei kann verarbeitet werden, um dieses Wort hervorzuheben, z. B. durch eine Fett\- oder Kursivformatierung.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit ["\/doc"](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#7)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Empfohlene Tags für Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)