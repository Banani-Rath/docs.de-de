---
title: "&lt;exception&gt; (Visual Basic) | Microsoft Docs"
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
  - "<exception> XML tag"
  - "exception XML tag"
ms.assetid: c0517549-171e-4dae-ab88-a9c1700b6eee
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;exception&gt; (Visual Basic)
Gibt an, welche Ausnahmen ausgelöst werden können.  
  
## Syntax  
  
```  
<exception cref="member">description</exception>  
```  
  
#### Parameter  
 `member`  
 ein Verweis auf eine Ausnahme, die in der aktuellen Kompilierungsumgebung verfügbar ist.  Der Compiler überprüft, ob die angegebene Ausnahme vorhanden ist, und übersetzt `member` in den in der XML\-Ausgabe enthaltenen kanonischen Elementnamen.  `member` muss in doppelte Anführungszeichen \(" "\) eingeschlossen werden.  
  
 `description`  
 eine Beschreibung.  
  
## Hinweise  
 Geben Sie mit dem `<exception>`\-Tag an, welche Ausnahmen ausgelöst werden können.  Dieses Tag wird auf eine Methodendefinition angewendet.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## Beispiel  
 In diesem Beispiel wird mit dem `<exception>`\-Tag eine Ausnahme beschrieben, die von der `IntDivide`\-Funktion ausgelöst werden kann.  
  
 [!CODE [VbVbcnXmlDocComments#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#3)]  
  
## Siehe auch  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)