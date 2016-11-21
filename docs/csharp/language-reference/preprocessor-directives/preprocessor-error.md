---
title: "#error (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "#error"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "#error-Direktive [C#]"
ms.assetid: f2a7f3af-4cf9-4111-b369-70204d24b26b
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# #error (C#-Referenz)
Mit `#error` kann ein Fehler an einer bestimmten Stelle des Codes generiert werden.  Beispiele:  
  
```  
#error Deprecated code in this method.  
```  
  
## Hinweise  
 `#error` wird häufig in bedingten Direktiven verwendet.  
  
 Es ist ebenfalls möglich, eine benutzerdefinierte Warnung mit [\#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md) zu generieren.  
  
## Beispiel  
  
```  
// preprocessor_error.cs  
// CS1029 expected  
#define DEBUG  
class MainClass   
{  
    static void Main()   
    {  
#if DEBUG  
#error DEBUG is defined  
#endif  
    }  
}  
```  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Präprozessordirektiven](../../../csharp/language-reference/preprocessor-directives/index.md)