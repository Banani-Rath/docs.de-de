---
title: "AddHandler Statement | Microsoft Docs"
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
  - "vb.AddHandlerMethod"
  - "addhandler"
  - "vb.addhandler"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "AddHandler statement"
ms.assetid: cfe69799-2a0f-42c0-a99e-09fed954da01
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# AddHandler Statement
Ordnet einem Ereignishandler zur Laufzeit ein Ereignis zu.  
  
## Syntax  
  
```  
AddHandler event, AddressOf eventhandler  
```  
  
## Teile  
 `event`  
 Der Name des zu behandelnden Ereignisses.  
  
 `eventhandler`  
 Der Name einer Prozedur zum Behandeln des Ereignisses.  
  
## Hinweise  
 Mit den Anweisungen `AddHandler` und `RemoveHandler` können Sie die Ereignisbehandlung an einer beliebigen Stelle in der Programmausführung starten und anhalten.  
  
 Die Signatur der `eventhandler`\-Prozedur muss mit der Signatur des Ereignisses `event` übereinstimmen.  
  
 Sie können sowohl mit dem `Handles`\-Schlüsselwort als auch mit der `AddHandler`\-Anweisung angeben, dass bestimmte Prozeduren bestimmte Ereignisse behandeln, doch weisen die beiden Verfahren Unterschiede auf.  Die `AddHandler`\-Anweisung verbindet zur Laufzeit Prozeduren mit Ereignissen.  Verwenden Sie das `Handles`\-Schlüsselwort beim Definieren einer Prozedur, um anzugeben, dass sie ein bestimmtes Ereignis behandelt.  Weitere Informationen finden Sie unter [Handles](../../../visual-basic/language-reference/statements/handles-clause.md).  
  
> [!NOTE]
>  Für benutzerdefinierte Ereignisse ruft die `AddHandler`\-Anweisung den `AddHandler`\-Accessor des Ereignisses auf.  Weitere Informationen über benutzerdefinierte Ereignisse finden Sie unter [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).  
  
## Beispiel  
 [!CODE [VbVbalrEvents#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#17)]  
  
## Siehe auch  
 [RemoveHandler Statement](../../../visual-basic/language-reference/statements/removehandler-statement.md)   
 [Handles](../../../visual-basic/language-reference/statements/handles-clause.md)   
 [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md)   
 [Events](../../../visual-basic/programming-guide/language-features/events/events.md)