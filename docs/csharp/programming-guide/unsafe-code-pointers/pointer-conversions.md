---
title: "Zeigerkonvertierungen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Zeiger [C#], Konvertierungen"
ms.assetid: f0e87502-477a-4ede-a31f-7a3e262e46fb
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Zeigerkonvertierungen (C#-Programmierhandbuch)
Die folgende Tabelle zeigt die vordefinierten impliziten Zeigerkonvertierungen.  Implizite Konvertierungen können in zahlreichen Situationen auftreten, z. B. in Methodenaufrufen und Zuweisungsanweisungen.  
  
## Implizite Zeigerkonvertierungen  
  
|Von|To|  
|---------|--------|  
|Beliebiger Zeigertyp|void\*|  
|null|Beliebiger Zeigertyp|  
  
 Die explizite Zeigerkonvertierung mithilfe von Typumwandlungsausdrücken wird für Konvertierungen verwendet, für die keine implizite Konvertierung vorhanden ist.  Diese Konvertierungen sind in der folgenden Tabelle zusammengefasst.  
  
## Explizite Zeigerkonvertierungen  
  
|Von|To|  
|---------|--------|  
|Beliebiger Zeigertyp|Alle anderen Zeigertypen|  
|sbyte, byte, short, ushort, int, uint, long oder ulong|Beliebiger Zeigertyp|  
|Beliebiger Zeigertyp|sbyte, byte, short, ushort, int, uint, long oder ulong|  
  
## Beispiel  
 Im folgenden Beispiel wird ein Zeiger auf `int` in einen Zeiger auf `byte` konvertiert.  Beachten Sie, dass der Zeiger auf das niedrigste adressierte Byte der Variablen zeigt.  Wenn Sie das Ergebnis schrittweise auf die Größe von `int` \(4 Bytes\) erhöhen, können Sie die verbleibenden Bytes der Variablen anzeigen.  
  
 [!CODE [csProgGuidePointers#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#3)]  
  
 [!CODE [csProgGuidePointers#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#4)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Zeigerausdrücke](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)   
 [Zeigertypen](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)   
 [Typen](../../../csharp/language-reference/keywords/types.md)   
 [Unsicher](../../../csharp/language-reference/keywords/unsafe.md)   
 [fixed\-Anweisung](../../../csharp/language-reference/keywords/fixed-statement.md)   
 [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)