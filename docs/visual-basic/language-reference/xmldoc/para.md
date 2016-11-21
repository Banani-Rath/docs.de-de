---
title: "&lt;para&gt; (Visual Basic) | Microsoft Docs"
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
  - "<para> XML tag"
  - "para XML tag"
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;para&gt; (Visual Basic)
Gibt an, dass der Inhalt als Absatz formatiert wird.  
  
## Syntax  
  
```  
<para>content</para>  
```  
  
#### Parameter  
 `content`  
 Der Text des Absatzes.  
  
## Hinweise  
 Das `<para>`\-Tag ist für die Verwendung innerhalb eines Tags, z. B. [\<summary\>](../../../visual-basic/language-reference/xmldoc/summary.md), [\<remarks\>](../../../visual-basic/language-reference/xmldoc/remarks.md) oder [\<returns\>](../../../visual-basic/language-reference/xmldoc/returns.md), vorgesehen. Sie können den Text damit strukturieren.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 Im folgenden Beispiel wird mit dem `<para>`\-Tag der Anmerkungsabschnitt für die `UpdateRecord`\-Methode in zwei Absätze aufgeteilt.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)