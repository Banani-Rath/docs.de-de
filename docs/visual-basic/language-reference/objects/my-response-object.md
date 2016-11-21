---
title: "My.Response Object | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "My.MyWebExtension.Response"
  - "My.Response"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Response object"
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# My.Response Object
Ruft das <xref:System.Web.HttpResponse>\-Objekt ab, das der <xref:System.Web.UI.Page> zugeordnet ist.  Dieses Objekt ermöglicht das Senden von HTTP\-Antwortdaten an einen Client und enthält Informationen über diese Antwort.  
  
## Hinweise  
 Das `My.Response`\-Objekt enthält das aktuelle <xref:System.Web.HttpResponse>\-Objekt, das der Seite zugeordnet ist.  
  
 Das `My.Response`\-Objekt ist nur für [!INCLUDE[vstecasp](../../../csharp/language-reference/preprocessor-directives/includes/vstecasp_md.md)]\-Anwendungen verfügbar.  
  
## Beispiel  
 Im folgenden Beispiel wird die Headerauflistung vom `My.Request`\-Objekt abgerufen, und das `My.Response`\-Objekt wird zum Schreiben der Auflistung in die ASP.NET\-Seite verwendet.  
  
 [!CODE [VbVbalrMyWeb#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyWeb#1)]  
  
## Siehe auch  
 <xref:System.Web.HttpResponse>   
 [My.Request Object](../../../visual-basic/language-reference/objects/my-request-object.md)