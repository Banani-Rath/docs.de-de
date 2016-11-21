---
title: "&#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39; | Microsoft Docs"
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
  - "vbc32096"
  - "bc32096"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC32096"
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39;
In einer `For Each`\-Anweisung wird eine Iteratorvariable angegeben, die über mehrere <xref:System.Collections.IEnumerable.GetEnumerator%2A>\-Methoden verfügt.  
  
 Die Iteratorvariable muss von einem Typ sein, der die <xref:System.Collections.IEnumerable?displayProperty=fullName>\-Schnittstelle oder die <xref:System.Collections.Generic.IEnumerable%601?displayProperty=fullName>\-Schnittstelle in einem der `Collections`\-Namespaces von [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] implementiert.  Eine Klasse kann mehrere erstellte generische Schnittstellen implementieren, wenn für jede erstellte Schnittstelle ein anderes Typargument verwendet wird.  Wenn eine Klasse, auf die diese Bedingungen zutreffen, für die Iteratorvariable verwendet wird, verfügt diese Variable über mehrere <xref:System.Collections.IEnumerable.GetEnumerator%2A>\-Methoden.  In solch einem Fall kann [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] nicht bestimmen, welche Methode aufgerufen werden soll.  
  
 **Fehler\-ID:** BC32096  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie [DirectCast Operator](../../../visual-basic/language-reference/operators/directcast-operator.md) oder [TryCast Operator](../../../visual-basic/language-reference/operators/trycast-operator.md), um den Typ der Iteratorvariablen in die Schnittstelle umzuwandeln, die die zu verwendende <xref:System.Collections.IEnumerable.GetEnumerator%2A>\-Methode definiert.  
  
## Siehe auch  
 [For Each...Next\-Anweisung](../../../visual-basic/language-reference/statements/for-each-next-statement.md)   
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)