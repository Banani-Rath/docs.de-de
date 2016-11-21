---
title: "remove (C#-Referenz) | Microsoft Docs"
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
  - "remove_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Remove-Ereignisaccessor [C#]"
ms.assetid: c8223426-c17b-4fe2-8406-01564cf1dd2b
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# remove (C#-Referenz)
Mit dem `remove`\-Kontextschlüsselwort wird ein benutzerdefinierter Ereignisaccessor definiert, der aufgerufen wird, wenn das Abonnement für das [Ereignis](../../../csharp/language-reference/keywords/event.md) durch Clientcode gekündigt wird.  Wenn Sie einen benutzerdefinierten `remove`\-Accessor angeben, müssen Sie auch einen [add](../../../csharp/language-reference/keywords/add.md)\-Accessor angeben.  
  
## Beispiel  
 Im folgenden Beispiel wird ein Ereignis mit einem benutzerdefinierten [add](../../../csharp/language-reference/keywords/add.md)\-Accessor und einem benutzerdefinierten `remove`\-Accessor veranschaulicht.  Das vollständige Beispiel finden Sie unter [Gewusst wie: Implementieren von Schnittstellenereignissen](../../../csharp/programming-guide/events/how-to-implement-interface-events.md).  
  
 [!CODE [csrefKeywordsContextual#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#15)]  
  
 Normalerweise müssen Sie keine eigenen benutzerdefinierten Ereignisaccessoren bereitstellen.  Die Accessoren, die vom Compiler beim Deklarieren eines Ereignisses automatisch generiert werden, sind in den meisten Szenarios ausreichend.  
  
## Siehe auch  
 [Ereignisse](../../../csharp/programming-guide/events/index.md)