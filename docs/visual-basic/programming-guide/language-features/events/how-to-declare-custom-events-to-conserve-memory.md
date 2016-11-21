---
title: "How to: Declare Custom Events To Conserve Memory (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "declaring events, custom"
  - "events [Visual Basic], custom"
  - "custom events"
ms.assetid: 87ebee87-260c-462f-979c-407874debd19
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Declare Custom Events To Conserve Memory (Visual Basic)
Unter gewissen Umständen muss die Speicherauslastung durch eine Anwendung gering gehalten werden.  Mit benutzerdefinierten Ereignissen wird es einer Anwendung ermöglicht, Speicher nur für die Ereignisse zu nutzen, die sie behandelt.  
  
 Wenn eine Klasse ein Ereignis deklariert, belegt der Compiler standardmäßig Speicher für ein Feld, in dem Ereignisinformationen gespeichert werden.  Wenn eine Klasse viele nicht verwendete Ereignisse aufweist, beanspruchen diese unnötigerweise Speicher.  
  
 Statt die von Visual Basic bereitgestellte Standardimplementierung von Ereignissen zu verwenden, können Sie die Speicherauslastung mithilfe benutzerdefinierter Ereignisse sorgfältiger verwalten.  
  
## Beispiel  
 In diesem Beispiel verwendet die Klasse eine Instanz der <xref:System.ComponentModel.EventHandlerList>\-Klasse, die im `Events`\-Feld gespeichert ist, um Informationen über die gegenwärtig verwendeten Ereignisse zu speichern.  Die <xref:System.ComponentModel.EventHandlerList>\-Klasse ist eine optimierte Listenklasse zum Speichern von Delegaten.  
  
 Alle Ereignisse in der Klasse verwenden das `Events`\-Feld, um nachzuverfolgen, welche Methoden jedes einzelne Ereignis behandeln.  
  
 [!CODE [VbVbalrEvents#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#22)]  
  
## Siehe auch  
 <xref:System.ComponentModel.EventHandlerList>   
 [Events](../../../../visual-basic/programming-guide/language-features/events/events.md)   
 [How to: Declare Custom Events To Avoid Blocking](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-avoid-blocking.md)