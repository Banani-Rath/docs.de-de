---
title: "Verwenden von Konvertierungsoperatoren (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Konvertierungsoperatoren [C#]"
  - "Konvertierungen [C#], Operatoren"
  - "Explizite Konvertierungsoperatoren [C#]"
  - "Implizite Konvertierungsoperatoren [C#]"
  - "Operatoren [C#], Konvertierung"
  - "Benutzerdefinierte Konvertierungen [C#]"
ms.assetid: caf36e89-c6c0-4b87-9f9e-85780a45c9a4
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Verwenden von Konvertierungsoperatoren (C#-Programmierhandbuch)
Sie können die einfacheren `implicit`\-Konvertierungsoperatoren verwenden oder die `explicit`\-Konvertierungsoperatoren, die eindeutig signalisieren, dass ein Typ konvertiert wird.  In diesem Thema werden beide Typen von Konvertierungsoperatoren veranschaulicht.  
  
> [!NOTE]
>  Weitere Informationen über einfache Typkonvertierungen finden Sie unter [Gewusst wie: Konvertieren einer Zeichenfolge in eine Zahl](../../../csharp/programming-guide/types/how-to-convert-a-string-to-a-number.md), [Gewusst wie: Konvertieren eines Bytearrays in einen ganzzahligen Typ](../../../csharp/programming-guide/types/how-to-convert-a-byte-array-to-an-int.md), [Gewusst wie: Konvertieren zwischen Hexadezimalzeichenfolgen und numerischen Typen](../../../csharp/programming-guide/types/how-to-convert-between-hexadecimal-strings-and-numeric-types.md) oder <xref:System.Convert>.  
  
## Beispiel  
 Dies ist ein Beispiel eines expliziten Konvertierungsoperators.  Dieser Operator konvertiert den Typ <xref:System.Byte> in den Wertetyp `Digit`.  Da nicht alle Bytes in eine Ziffer konvertiert werden können, ist die Konvertierung explizit. Das bedeutet, dass eine Umwandlung verwendet werden muss, wie in der `Main`\-Methode dargestellt wird.  
  
 [!CODE [csProgGuideStatements#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#11)]  
  
## Beispiel  
 In diesem Beispiel wird ein impliziter Konvertierungsoperator dargestellt. Es wird ein Konvertierungsoperator definiert, der das Ergebnis des vorherigen Beispiels rückgängig macht: Er konvertiert die Wertklasse `Digit` in den ganzzahligen Typ <xref:System.Byte>.  Da sich alle Ziffern in ein <xref:System.Byte> konvertieren lassen, besteht kein Anlass, die explizite Konvertierung zu erzwingen.  
  
 [!CODE [csProgGuideStatements#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#12)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)   
 [is](../../../csharp/language-reference/keywords/is.md)