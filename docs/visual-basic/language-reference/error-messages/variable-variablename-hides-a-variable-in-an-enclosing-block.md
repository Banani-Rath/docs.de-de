---
title: "Variable &#39;&lt;variablename&gt;&#39; hides a variable in an enclosing block | Microsoft Docs"
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
  - "vbc30616"
  - "bc30616"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30616"
ms.assetid: e7658ebc-da45-451b-a409-a0f8915f0beb
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Variable &#39;&lt;variablename&gt;&#39; hides a variable in an enclosing block
Eine in einen Block eingeschlossene Variable hat denselben Namen wie eine andere lokale Variable.  
  
 **Fehler\-ID:** BC30616  
  
### So beheben Sie diesen Fehler  
  
-   Benennen Sie die Variable im betreffenden Block um, sodass der Name nicht mit dem Namen anderer lokaler Variablen identisch ist.  Beispiele:  
  
    ```  
    Dim a, b, x As Integer  
    If a = b Then  
       Dim y As Integer = 20 ' Uniquely named block variable.  
    End If  
    ```  
  
-   Eine häufige Ursache für diesen Fehler ist die Verwendung von `Catch e As Exception` innerhalb eines Ereignishandlers.  Wenn dies der Fall ist, nennen Sie die Variable des `Catch`\-Blocks `ex` und nicht `e`.  
  
-   Ein weiterer häufiger Auslöser für diesen Fehler ist der Versuch, auf eine lokale Variable zuzugreifen, die innerhalb eines `Try`\-Blocks in einem separaten `Catch`\-Block deklariert ist.  Um diesen Fehler zu beheben, deklarieren Sie die Variable außerhalb der `Try...Catch...Finally`\-Struktur.  
  
## Siehe auch  
 [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)   
 [Variablendeklaration](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)