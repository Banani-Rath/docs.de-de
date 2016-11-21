---
title: "&#39;&lt;typename&gt;&#39; is a delegate type | Microsoft Docs"
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
  - "bc32008"
  - "vbc32008"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC32008"
ms.assetid: dc6abba0-a9ad-450f-8899-87265bc84abc
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;typename&gt;&#39; is a delegate type
"\<Typname\>" ist ein Delegattyp.Für das Erstellen eines Delegaten kann nur ein einziger AddressOf\-Ausdruck als Argument übergeben werden.In vielen Fällen kann ein AddressOf\-Ausdruck anstelle einer Delegatkonstruktion verwendet werden.  
  
 Eine `New`\-Klausel, die eine Instanz einer Delegatklasse erstellt, gibt dem Delegatkonstruktor eine ungültige Argumentliste an.  
  
 Sie können beim Erstellen einer neuen Delegatinstanz nur einen einzigen `AddressOf`\-Ausdruck bereitstellen.  
  
 Dieser Fehler kann auftreten, wenn Sie an den Delegatkonstruktor keine Argumente, mehr als ein Argument oder ein einzelnes Argument übergeben, das keinen gültigen `AddressOf`\-Ausdruck darstellt.  
  
 **Fehler\-ID:** BC32008  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie einen einzigen `AddressOf`\-Ausdruck in der Argumentliste für die Delegatklasse der `New`\-Klausel.  
  
## Siehe auch  
 [New Operator](../../../visual-basic/language-reference/operators/new-operator.md)   
 [AddressOf Operator](../../../visual-basic/language-reference/operators/addressof-operator.md)   
 [Delegates](../../../visual-basic/programming-guide/language-features/delegates/delegates.md)   
 [How to: Invoke a Delegate Method](../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)