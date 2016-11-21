---
title: "&lt;example&gt; (Visual Basic) | Microsoft Docs"
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
  - "example XML tag"
  - "<example> XML tag"
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;example&gt; (Visual Basic)
Gibt ein Beispiel für den Member an.  
  
## Syntax  
  
```  
<example>description</example>  
```  
  
#### Parameter  
 `description`  
 eine Beschreibung des Codebeispiels.  
  
## Hinweise  
 Mit dem `<example>`\-Tag kann ein Beispiel für die Verwendung einer Methode oder eines anderen Bibliothekmembers angegeben werden.  Dies beinhaltet im Allgemeinen die Verwendung des [\<code\>](../../../visual-basic/language-reference/xmldoc/code.md)\-Tags.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 In diesem Beispiel wird das `<example>`\-Tag verwendet, um ein Beispiel für die Verwendung des `ID`\-Feldes einzufügen.  
  
 [!CODE [VbVbcnXmlDocComments#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#2)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)