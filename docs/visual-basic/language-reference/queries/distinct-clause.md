---
title: "Distinct Clause (Visual Basic) | Microsoft Docs"
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
  - "vb.QueryDistinct"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Distinct clause"
  - "Distinct statement"
  - "queries [Visual Basic], Distinct"
ms.assetid: 86f42614-0d8f-4ffc-b888-ce8a37a8d36a
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Distinct Clause (Visual Basic)
Schränkt die Werte der aktuellen Bereichsvariable ein, um doppelte Werte in nachfolgenden Abfrageklauseln auszuschließen.  
  
## Syntax  
  
```  
Distinct  
```  
  
## Hinweise  
 Die `Distinct`\-Klausel kann verwendet werden, um eine Liste eindeutiger Elemente zurückzugeben.  Die `Distinct`\-Klausel veranlasst, dass bei der Abfrage doppelte Abfrageergebnisse ignoriert werden.  Die `Distinct`\-Klausel gilt für doppelte Werte aller von der `Select`\-Klausel angegebenen Rückgabefelder.  Wenn keine `Select`\-Klausel angegeben ist, hat die `Distinct`\-Klausel für die Bereichsvariable der Abfrage Gültigkeit, die in der `From`\-Klausel angegeben ist.  Falls die Bereichsvariable ein veränderlicher Typ ist, wird die Abfrage ein Abfrageergebnis nur ignorieren, wenn alle Mitglieder des Typs dem vorhandenen Abfrageergebnis entsprechen.  
  
## Beispiel  
 Der folgende Abfrageausdruck verknüpft eine Liste von Kunden mit einer Liste von Kundenbestellungen.  Die `Distinct`\-Klausel wird angegeben, um eine Liste von eindeutigen Kundennamen und Bestelldaten zurückzugeben.  
  
 [!CODE [VbSimpleQuerySamples#20](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#20)]  
  
## Siehe auch  
 [Introduction to LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)   
 [Queries](../../../visual-basic/language-reference/queries/queries.md)   
 [From Clause](../../../visual-basic/language-reference/queries/from-clause.md)   
 [Select Clause](../../../visual-basic/language-reference/queries/select-clause.md)   
 [Where Clause](../../../visual-basic/language-reference/queries/where-clause.md)