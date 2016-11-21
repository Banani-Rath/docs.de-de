---
title: "&lt;typeparam&gt; (Visual Basic) | Microsoft Docs"
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
  - "typeparam XML tag"
  - "<typeparam> XML tag"
ms.assetid: 1bb5ba78-f060-478c-905c-77a2e43639af
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;typeparam&gt; (Visual Basic)
Definiert einen Typparameternamen und eine Beschreibung.  
  
## Syntax  
  
```  
<typeparam name="name">description</typeparam>  
```  
  
#### Parameter  
 `name`  
 Der Name des Typparameters.  Der Name muss in doppelte Anführungszeichen \(**" "**\) eingeschlossen werden.  
  
 `description`  
 Eine Beschreibung des Typparameters.  
  
## Hinweise  
 Verwenden Sie das `<typeparam>`\-Tag im Kommentar für eine generische Typ\- oder Memberdeklaration, um einen der Typparameter zu beschreiben.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 In diesem Beispiel wird das `<typeparam>`\-Tag verwendet, um den `id`\-Parameter zu beschreiben.  
  
 [!CODE [VbVbcnXmlDocComments#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#8)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)