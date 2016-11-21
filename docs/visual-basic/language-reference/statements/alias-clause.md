---
title: "Alias Clause (Visual Basic) | Microsoft Docs"
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
  - "vb.Alias"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Alias keyword"
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Alias Clause (Visual Basic)
Gibt an, dass eine externe Prozedur in der DLL einen anderen Namen aufweist.  
  
## Hinweise  
 Das `Alias`\-Schlüsselwort kann im folgenden Kontext verwendet werden:  
  
 [Declare\-Anweisung](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 Im folgenden Beispiel wird mit dem `Alias`\-Schlüsselwort der Name der Funktion in "advapi32.dll" \(`GetUserNameA`\) angegeben, der von `getUserName` in diesem Beispiel verwendet wird.  Die `getUserName`\-Funktion wird in Sub `getUser` aufgerufen, wodurch der Name des aktuellen Benutzers angezeigt wird.  
  
 [!CODE [VbVbalrStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#15)]  
  
## Siehe auch  
 [Stichwörter](../../../visual-basic/language-reference/keywords/index.md)