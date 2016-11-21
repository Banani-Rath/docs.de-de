---
title: "&lt;c&gt; (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "c XML tag"
  - "<c> XML tag"
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;c&gt; (Visual Basic)
Gibt an, dass es sich bei Text innerhalb einer Beschreibung um Code handelt.  
  
## Syntax  
  
```  
<c>text</c>  
```  
  
#### Parameter  
  
|||  
|-|-|  
|Parameter|Beschreibung|  
|`text`|der Text, der als Code angegeben werden soll.|  
  
## Hinweise  
 Mit dem `<c>`\-Tag kann angegeben werden, dass Text in einer Beschreibung als Code gekennzeichnet werden soll.  Verwenden Sie [\<code\>](../../../visual-basic/language-reference/xmldoc/code.md), um mehrere Zeilen als Code anzugeben.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 In diesem Beispiel wird mit dem `<c>`\-Tag im Zusammenfassungsabschnitt angegeben, dass es sich bei `Counter` um Code handelt.  
  
 [!CODE [VbVbcnXmlDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#1)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)