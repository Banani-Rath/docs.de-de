---
title: "Gewusst wie: Gruppieren von Ergebnissen nach zusammenh&#228;ngenden Schl&#252;sseln (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Zusammenhängende Schlüssel [LINQ in C#]"
ms.assetid: 0f0f48a8-e13b-4274-8903-3b73f68cd18e
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Gruppieren von Ergebnissen nach zusammenh&#228;ngenden Schl&#252;sseln (C#-Programmierhandbuch)
Im folgenden Beispiel wird gezeigt, wie Elemente in Ausschnitte gruppiert werden, die Untersequenzen von zusammenhängenden Schlüsseln darstellen.  Angenommen, Sie erhalten die folgende Sequenz von Schlüssel\/Wert\-Paaren:  
  
|Schlüssel|Wert|  
|---------------|----------|  
|A|Wir|  
|A|denken|  
|A|that|  
|B|Linq|  
|C|entspricht|  
|A|cool|  
|B|ist|  
|B|\!|  
  
 Die folgenden Gruppen werden in dieser Reihenfolge erstellt:  
  
1.  Wir, denken, dass  
  
2.  Linq  
  
3.  entspricht  
  
4.  cool  
  
5.  ist, \!  
  
 Die Lösung wird als Erweiterungsmethode implementiert, die threadsicher ist und die Ergebnisse mit Streaming zurückgibt.  Mit anderen Worten: Sie erzeugt ihre Gruppen beim Durchlaufen der Quellsequenz.  Im Gegensatz zu den Operatoren `group` und `orderby` kann die Rückgabe von Gruppen an den Aufrufer beginnen, bevor alle Sequenzen gelesen wurden.  
  
 Die Threadsicherheit wird gewährleistet, indem eine Kopie einer Gruppe oder eines Abschnitts als Quellsequenz durchlaufen wird, wie in den Quellcodekommentaren erläutert.  Falls die Quellsequenz über eine große Sequenz von zusammenhängenden Elementen verfügt, löst die Common Language Runtime \(CLR\) eventuell eine <xref:System.OutOfMemoryException> aus.  
  
## Beispiel  
 Im folgenden Beispiel werden sowohl die Erweiterungsmethode als auch der Clientcode, in denen sie verwendet wird, veranschaulicht.  
  
 [!CODE [cscsrefContiguousGroups#1](../CodeSnippet/VS_Snippets_VBCSharp/cscsrefContiguousGroups#1)]  
  
 Um die Erweiterungsmethode in Ihrem Projekt zu verwenden, kopieren Sie die statische `MyExtensions`\-Klasse in eine neue oder bereits vorhandene Quellcodedatei und fügen Sie ggf. eine `using`\-Direktive für den Namespace an der Stelle hinzu, an der er sich befindet.  
  
## Siehe auch  
 [LINQ\-Abfrageausdrücke](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [Classification of Standard Query Operators by Manner of Execution](../../../visual-basic/programming-guide/concepts/linq/classification-of-standard-query-operators-by-manner-of-execution.md)