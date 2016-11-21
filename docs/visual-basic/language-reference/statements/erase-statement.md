---
title: "Erase Statement (Visual Basic) | Microsoft Docs"
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
  - "vb.Erase"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Erase keyword"
  - "Erase statement"
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Erase Statement (Visual Basic)
Wird zur Freigabe von Arrayvariablen und des Speichers, der für ihre Elemente benötigt wird, verwendet.  
  
## Syntax  
  
```  
Erase arraylist  
```  
  
## Teile  
 `arraylist`  
 Erforderlich.  Liste der zu löschenden Arrayvariablen.  Mehrere Variablen werden durch Komma voneinander getrennt.  
  
## Hinweise  
 Die `Erase`\-Anweisung kann nur auf Prozedurebene verwendet werden.  Das bedeutet, Sie können Arrays zwar in einer Prozedur freigeben, jedoch nicht auf Klassen\- oder Modulebene.  
  
 Statt die `Erase`\-Anweisung zu verwenden, können Sie den einzelnen Arrayvariablen auch `Nothing` zuweisen.  
  
## Beispiel  
 Im folgenden Beispiel werden mit der `Erase`\-Anweisung zwei Arrays gelöscht, und der von ihnen belegte Speicherplatz wird freigegeben \(jeweils 1000 bzw. 100 Speicherelemente\).  Anschließend weist die `ReDim`\-Anweisung dem dreidimensionalen Array eine neue Arrayinstanz zu.  
  
 [!CODE [VbVbalrStatements#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#19)]  
  
## Siehe auch  
 [Nothing](../../../visual-basic/language-reference/nothing.md)   
 [ReDim Statement](../../../visual-basic/language-reference/statements/redim-statement.md)