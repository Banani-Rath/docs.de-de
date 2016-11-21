---
title: "Stop Statement (Visual Basic) | Microsoft Docs"
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
  - "vb.Stop"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "breakpoints, Stop statements"
  - "Stop statements, syntax"
  - "Stop statements"
  - "execution, suspending"
  - "processing, interrupting"
  - "processes, interrupting"
  - "execution, stopping"
ms.assetid: c9a9fde0-d649-4662-9bef-bd0146ebc2a7
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Stop Statement (Visual Basic)
Unterbricht die Ausführung.  
  
## Syntax  
  
```  
Stop  
```  
  
## Hinweise  
 Sie können die `Stop`\-Anweisungen an einer beliebigen Stelle in Prozeduren verwenden, um die Ausführung zu unterbrechen.  Die `Stop`\-Anweisung entspricht dem Festlegen eines Haltepunkts in Code.  
  
 Die `Stop`\-Anweisung unterbricht die Ausführung, schließt aber im Gegensatz zu `End` keine Dateien und setzt auch keine Variablen zurück, es sei denn, die Anweisung befindet sich in einer kompilierten ausführbaren Datei \(EXE\-Datei\).  
  
> [!NOTE]
>  Wenn sich die `Stop`\-Anweisung in Code befindet, der außerhalb der IDE \(Integrated Development Environment\) ausgeführt wird, wird der Debugger aufgerufen.  Dabei spielt es keine Rolle, ob der Code im Debug\- oder im Retail\-Modus kompiliert wurde.  
  
## Beispiel  
 In diesem Beispiel wird die `Stop`\-Anweisung verwendet, um die Ausführung bei jedem Durchlauf der `For...Next`\-Schleife anzuhalten.  
  
 [!CODE [VbVbalrStatements#56](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#56)]  
  
## Siehe auch  
 [End Statement](../../../visual-basic/language-reference/statements/end-statement.md)