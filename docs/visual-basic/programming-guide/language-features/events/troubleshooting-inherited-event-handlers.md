---
title: "Troubleshooting Inherited Event Handlers in Visual Basic | Microsoft Docs"
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
  - "troubleshooting events"
  - "inherited events"
  - "troubleshooting Visual Basic, event handlers"
  - "event handling, troubleshooting"
  - "event handlers, troubleshooting"
ms.assetid: e1c8759f-5370-4308-8476-8c48b73509bf
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Troubleshooting Inherited Event Handlers in Visual Basic
Unter diesem Thema sind allgemeine Probleme aufgeführt, die sich bei Ereignishandlern in geerbten Komponenten ergeben.  
  
## Arbeitsschritte  
  
#### Code im Ereignishandler wird für jeden Aufruf zweimal ausgeführt  
  
-   Ein geerbter Ereignishandler darf keine [Handles](../../../../visual-basic/language-reference/statements/handles-clause.md)\-Klausel enthalten.  Die Methode in der Basisklasse ist bereits mit dem Ereignis verknüpft und wird entsprechend ausgelöst.  Entfernen Sie die `Handles`\-Klausel aus der geerbten Methode.  
  
     [!CODE [VbVbalrEvents#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#32)]  
  
-   Wenn die geerbte Methode kein `Handles`\-Schlüsselwort enthält, darf der Code nicht zusätzlich eine [AddHandler Statement](../../../../visual-basic/language-reference/statements/addhandler-statement.md) oder zusätzliche Methoden zum Behandeln desselben Ereignisses enthalten.  
  
## Siehe auch  
 [Events](../../../../visual-basic/programming-guide/language-features/events/events.md)