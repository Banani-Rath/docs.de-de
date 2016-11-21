---
title: "&#39;&lt;membername&gt;&#39; cannot expose type &#39;&lt;typename&gt;&#39; outside the project through &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39; | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30909"
  - "vbc30909"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30909"
ms.assetid: ffa7395d-e182-4087-8ce8-079810fdae54
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;membername&gt;&#39; cannot expose type &#39;&lt;typename&gt;&#39; outside the project through &lt;containertype&gt; &#39;&lt;containertypename&gt;&#39;
Eine Variable, ein Prozedurparameter oder eine Funktionsrückgabe wird außerhalb des zugehörigen Containers verfügbar gemacht, ist jedoch als Typ deklariert, der nicht außerhalb des Containers verfügbar gemacht werden darf.  
  
 Im folgenden Codeskelett wird eine Situation veranschaulicht, die diesen Fehler generiert.  
  
```  
Private Class privateClass  
End Class  
Public Class mainClass  
    Public exposedVar As New privateClass  
End Class  
```  
  
 Ein als `Protected`, `Friend`, `Protected Friend` oder `Private` deklarierter Typ soll außerhalb des Deklarationskontexts eingeschränkten Zugriff aufweisen.  Dies ist nicht möglich, wenn er als Datentyp einer Variablen mit weniger eingeschränktem Zugriff verwendet wird.  Im vorhergehenden Skelettcode ist `exposedVar` `Public` und macht `privateClass` für Code verfügbar, der nicht darauf zugreifen soll.  
  
 **Fehler\-ID:** BC30909  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie die Zugriffsebene der Variablen, des Prozedurparameters oder der Funktionsrückgabe in eine Zugriffsebene, die mindestens so restriktiv wie die Zugriffsebene des zugehörigen Datentyps ist.  
  
## Siehe auch  
 [Access Levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)