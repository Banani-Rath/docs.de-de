---
title: "Gewusst wie: Verwenden der Operator&#252;berladung zum Erstellen einer Klasse f&#252;r komplexe Zahlen (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Klassen [C#], Operatoren überladen"
  - "Komplexe Zahlen [C#]"
  - "Überladen von Operatoren [C#], Komplexe Zahlen"
  - "Überladen von Operatoren [C#], Verwenden zum Erstellen von Klassen"
  - "Operatoren [C#], Überladen zum Erstellen einer komplexen Zahlenklasse"
ms.assetid: c9b8d982-5112-413f-bae3-b42ae3248ddf
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden der Operator&#252;berladung zum Erstellen einer Klasse f&#252;r komplexe Zahlen (C#-Programmierhandbuch)
In diesem Beispiel erfahren Sie, wie Sie überladene Operatoren verwenden können, um eine Klasse für komplexe Zahlen, `Complex`, zu erstellen, durch die komplexe Additionen definiert werden.  Das Programm zeigt den imaginären und den realen Teil der Zahlen an. Das Additionsergebnis wird mittels einer Überschreibung der `ToString`\-Methode dargestellt.  
  
## Beispiel  
 [!CODE [csProgGuideStatements#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#16)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)   
 [Operator](../../../csharp/language-reference/keywords/operator.md)   
 [Warum sind überladene Operatoren in C\# immer statisch?](http://go.microsoft.com/fwlink/?LinkId=112383)