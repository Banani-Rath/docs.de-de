---
title: "Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39; | Microsoft Docs"
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
  - "vbc40007"
  - "bc40007"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC40007"
ms.assetid: 692ccf76-5715-4f11-a972-84cf9de30bc1
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Default property &#39;&lt;propertyname1&gt;&#39; conflicts with default property &#39;&lt;propertyname2&gt;&#39; in &#39;&lt;classname&gt;&#39; and so should be declared &#39;Shadows&#39;
Es wurde eine Eigenschaft mit dem Namen einer Eigenschaft in der Basisklasse deklariert.  In dieser Situation muss die Eigenschaft in dieser Klasse ein Shadowing über die Eigenschaft der Basisklasse ausführen.  
  
 Bei dieser Meldung handelt es sich um eine Warnung.  `Shadows` wird standardmäßig angenommen.  Weitere Informationen über das Ausblenden von Warnungen bzw. über die Behandlung von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](/visual-studio/ide/configuring-warnings-in-visual-basic).  
  
 **Fehler\-ID:** BC40007  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie das `Shadows`\-Schlüsselwort zur Deklaration hinzu, oder ändern Sie den Namen der Eigenschaft, die deklariert wird.  
  
## Siehe auch  
 [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md)   
 [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)