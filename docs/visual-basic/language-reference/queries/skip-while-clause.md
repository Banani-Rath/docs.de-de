---
title: "Skip While Clause (Visual Basic) | Microsoft Docs"
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
  - "vb.QuerySkipWhile"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Skip While statement"
  - "Skip While clause"
  - "queries [Visual Basic], Skip While"
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Skip While Clause (Visual Basic)
Überspringt Elemente in einer Auflistung, solange eine angegebene Bedingung `true` ist, und gibt anschließend die übrigen Elemente zurück.  
  
## Syntax  
  
```  
Skip While expression  
```  
  
## Teile  
  
|||  
|-|-|  
|Begriff|Definition|  
|`expression`|Erforderlich.  Ein Ausdruck, der eine Bedingung darstellt, auf die Elemente getestet werden sollen.  Der Ausdruck muss einen `Boolean`\-Wert oder eine funktionale Entsprechung wie beispielsweise einen `Integer`\-Wert zurückgeben, um als `Boolean` ausgewertet zu werden.|  
  
## Hinweise  
 Mit der `Skip While`\-Klausel werden Elemente zu Beginn eines Abfrageergebnisses übersprungen, bis vom bereitgestellten `expression` der Wert `false` zurückgegeben wird  Sobald von `expression` der Wert `false` zurückgegeben wird, werden alle übrigen Elemente von der Abfrage zurückgegeben.  Für die übrigen Ergebnisse wird `expression` ignoriert.  
  
 Die `Skip While`\-Klausel unterscheidet sich von der `Where`\-Klausel insofern, als mit der `Where`\-Klausel alle Elemente, die eine bestimmte Bedingung nicht erfüllen, aus einer Abfrage ausgeschlossen werden können.  Mit der `Skip While`\-Klausel werden Elemente nur so lange ausgeschlossen, bis diese Bedingung zum ersten Mal nicht erfüllt wird.  Die `Skip While`\-Klausel ist besonders hilfreich, wenn Sie mit einem sortierten Abfrageergebnis arbeiten.  
  
 Mithilfe der `Skip`\-Klausel können Sie eine bestimmte Anzahl von Ergebnissen zu Beginn eines Abfrageergebnisses überspringen.  
  
## Beispiel  
 Im folgenden Codebeispiel werden mit der `Skip While`\-Klausel Ergebnisse übersprungen, bis der erste Kunde aus den USA gefunden wird.  
  
 [!CODE [VbSimpleQuerySamples#3](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#3)]  
  
## Siehe auch  
 [Introduction to LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)   
 [Queries](../../../visual-basic/language-reference/queries/queries.md)   
 [Select Clause](../../../visual-basic/language-reference/queries/select-clause.md)   
 [From Clause](../../../visual-basic/language-reference/queries/from-clause.md)   
 [Skip Clause](../../../visual-basic/language-reference/queries/skip-clause.md)   
 [Take While Clause](../../../visual-basic/language-reference/queries/take-while-clause.md)   
 [Where Clause](../../../visual-basic/language-reference/queries/where-clause.md)