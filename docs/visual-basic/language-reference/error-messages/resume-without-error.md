---
title: "Resume without error | Microsoft Docs"
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
  - "vbrID20"
dev_langs: 
  - "VB"
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Resume without error
Es wurde eine `Resume`\-Anweisung außerhalb des Fehlerbehandlungscodes gefunden, oder die Codeausführung ist in einen Fehlerhandler gesprungen, obwohl kein Fehler aufgetreten war.  
  
### So beheben Sie diesen Fehler  
  
1.  Verschieben Sie die `Resume`\-Anweisung in einen Fehlerhandler, oder löschen Sie sie.  
  
2.  Da Sprünge in Bezeichnungen nicht prozedurübergreifend erfolgen können, sollten Sie in der Prozedur nach der Bezeichnung suchen, durch die der Fehlerhandler identifiziert wird.  Falls Sie zwei Bezeichnungen finden, die das Ziel einer `GoTo`\-Anweisung darstellen, die jedoch keine `On Error GoTo`\-Anweisung ist, ändern Sie die Zeilenbezeichnung in das beabsichtigte Ziel.  
  
## Siehe auch  
 [Resume Statement](../../../visual-basic/language-reference/statements/resume-statement.md)   
 [On Error Statement](../../../visual-basic/language-reference/statements/on-error-statement.md)