---
title: "&lt;typeparam&gt; (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "typeparam"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<typeparam> (C#-XML-Tag)"
  - "typeparam (C#-XML-Tag)"
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &lt;typeparam&gt; (C#-Programmierhandbuch)
## Syntax  
  
```  
<typeparam name="name">description</typeparam>  
```  
  
#### Parameter  
 `name`  
 Der Name des Typparameters.  Der Name muss in doppelte Anführungszeichen \(**" "**\) eingeschlossen werden.  
  
 `description`  
 Eine Beschreibung für den Typparameter.  
  
## Hinweise  
 Das `<typeparam>`\-Tag sollte in dem Kommentar für einen generischen Typ oder eine Methodendeklaration zum Beschreiben eines Typparameters verwendet werden.  Fügen Sie für jeden Typparameter des generischen Typs oder der Methode ein Tag hinzu.  
  
 Weitere Informationen finden Sie unter [Generika](../../../csharp/programming-guide/generics/index.md).  
  
 Der Text für das `<typeparam>`\-Tag wird in IntelliSense, dem [Object Browser Window](http://msdn.microsoft.com/de-de/3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda)\-Webbericht für Codekommentare, angezeigt.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit ["\/doc"](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#13)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Empfohlene Tags für Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)