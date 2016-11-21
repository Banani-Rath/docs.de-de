---
title: "XML comment exception must have a &#39;cref&#39; attribute | Microsoft Docs"
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
  - "bc42319"
  - "vbc42319"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC42319"
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML comment exception must have a &#39;cref&#39; attribute
Das \< exception \>\-Tag bietet eine Möglichkeit zur Dokumentation der Ausnahmen, die von einer Methode ausgelöst werden können.  Das erforderliche `cref`\-Attribut legt den Namen eines Members fest, der vom Dokumentationsgenerator überprüft wird.  Wenn der Member vorhanden ist, wird er in der Dokumentationsdatei in den kanonischen Elementnamen übersetzt.  
  
 **Fehler\-ID:** BC42319  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie das `cref`\-Attribut der Ausnahme wie folgt hinzu:  
  
    ```  
    '''<exception cref="member">description</exception>  
    ```  
  
## Siehe auch  
 [\<exception\>](../../../visual-basic/language-reference/xmldoc/exception.md)   
 [How to: Create XML Documentation](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)   
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)