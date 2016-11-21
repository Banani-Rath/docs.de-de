---
title: "Statement is not valid inside a method/multiline lambda | Microsoft Docs"
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
  - "vbc30024"
  - "bc30024"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30024"
ms.assetid: 758e7a8f-429b-42c1-9a78-778e5b480e04
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Statement is not valid inside a method/multiline lambda
Die Anweisung ist innerhalb einer `Sub`\-Prozedur oder `Function`\-Prozedur sowie einer `Get`\-Eigenschaftenprozedur oder `Set`\-Eigenschaftenprozedur nicht gültig.  Einige Anweisungen können auf Modul\- oder Klassenebene definiert werden.  Andere Anweisungen wie z. B. `Option Strict` müssen auf Namespaceebene definiert werden und allen anderen Deklarationen vorangehen.  
  
 **Fehler\-ID:** BC30024  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie die Anweisung aus der Prozedur.  
  
## Siehe auch  
 [Sub Statement](../../../visual-basic/language-reference/statements/sub-statement.md)   
 [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md)   
 [Get Statement](../../../visual-basic/language-reference/statements/get-statement.md)   
 [Set Statement](../../../visual-basic/language-reference/statements/set-statement.md)