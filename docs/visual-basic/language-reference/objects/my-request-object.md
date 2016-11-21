---
title: "My.Request Object | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "My.MyWebExtension.Request"
  - "My.Request"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Request object"
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# My.Request Object
Ruft das <xref:System.Web.HttpRequest>\-Objekt für die angeforderte Seite ab.  
  
## Hinweise  
 Das `My.Request`\-Objekt enthält Informationen über die aktuelle HTTP\-Anforderung.  
  
 Das `My.Request`\-Objekt ist nur für ASP.NET\-Anwendungen verfügbar.  
  
## Beispiel  
 Im folgenden Beispiel wird die Headerauflistung vom `My.Request`\-Objekt abgerufen, und das `My.Response`\-Objekt wird zum Schreiben der Auflistung in die ASP.NET\-Seite verwendet.  
  
 [!CODE [VbVbalrMyWeb#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyWeb#1)]  
  
## Siehe auch  
 <xref:System.Web.HttpRequest>   
 [My.Response Object](../../../visual-basic/language-reference/objects/my-response-object.md)