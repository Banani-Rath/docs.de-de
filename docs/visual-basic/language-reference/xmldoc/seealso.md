---
title: "&lt;seealso&gt; (Visual Basic) | Microsoft Docs"
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
  - "<seealso> XML tag"
  - "seealso XML tag"
ms.assetid: 36050c95-1af2-4284-b9b6-1a70691ed978
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;seealso&gt; (Visual Basic)
Gibt einen Link an, der im Abschnitt Siehe auch angezeigt wird.  
  
## Syntax  
  
```  
<seealso cref="member"/>  
```  
  
#### Parameter  
 `member`  
 Ein Verweis auf einen Member oder ein Feld, der bzw. das von der aktuellen Kompilierungsumgebung aufgerufen werden kann.  Der Compiler überprüft, ob das angegebene Codeelement vorhanden ist, und übergibt `member` an den Elementnamen in der XML\-Ausgabe.  `member` muss in doppelte Anführungszeichen \(" "\) eingeschlossen werden.  
  
## Hinweise  
 Geben Sie mit dem `<seealso>`\-Tag den Text an, der in einem Siehe auch\-Abschnitt angezeigt werden soll.  Mit [\<see\>](../../../visual-basic/language-reference/xmldoc/see.md) wird ein Link im Text angegeben.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 In diesem Beispiel verweist das `<seealso>`\-Tag im `DoesRecordExist`\-Hinweisabschnitt auf die `UpdateRecord`\-Methode.  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)