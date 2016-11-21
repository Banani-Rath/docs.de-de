---
title: "&lt;permission&gt; (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "permission"
  - "<permission>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<permission> (C#-XML-Tag)"
  - "permission (C#-XML-Tag)"
ms.assetid: 769e93fe-8404-443f-bf99-577aa42b6a49
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &lt;permission&gt; (C#-Programmierhandbuch)
## Syntax  
  
```  
<permission cref="member">description</permission>  
```  
  
#### Parameter  
 cref \= "`member`"  
 Ein Verweis auf einen Member oder ein Feld, der bzw. das von der aktuellen Kompilierungsumgebung aufgerufen werden kann.  Der Compiler überprüft, ob das angegebene Codeelement vorhanden ist, und übersetzt `member` in den kanonischen Elementnamen in der ausgegebenen XML.  *member* muss in doppelte Anführungszeichen \(" "\) eingeschlossen werden.  
  
 Informationen für das Erstellen von cref\-Verweisen auf einen generischen Typ finden Sie unter [\<see\>](../../../csharp/programming-guide/xmldoc/see.md).  
  
 `description`  
 Eine Beschreibung des Zugriffs auf den Member.  
  
## Hinweise  
 Mit dem \<permission\>\-Tag kann der Zugriff auf einen Member dokumentiert werden.  Den Zugriff auf einen Member können Sie mithilfe der <xref:System.Security.PermissionSet>\-Klasse angeben.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit ["\/doc"](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#8)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Empfohlene Tags für Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)