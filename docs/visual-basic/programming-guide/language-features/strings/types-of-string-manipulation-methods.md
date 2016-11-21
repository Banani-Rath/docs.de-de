---
title: "Types of String Manipulation Methods in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "strings [Visual Basic], manipulating [Visual Basic]"
  - "string manipulation"
ms.assetid: 905055cd-7f50-48fb-9eed-b0995af1dc1f
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Types of String Manipulation Methods in Visual Basic
Zum Analysieren und Bearbeiten von Zeichenfolgen gibt es verschiedene Möglichkeiten.  Einige dieser Methoden sind Bestandteil der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Sprache, wohingegen andere Bestandteil der `String`\-Klasse sind.  
  
## Visual Basic und .NET Framework  
 [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Methoden werden als inhärente Funktionen der Sprache verwendet.  Sie können im Code ohne Qualifizierung verwendet werden.  Im folgenden Beispiel wird die typische Verwendung eines [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Befehls zur Zeichenfolgenbearbeitung veranschaulicht:  
  
 [!CODE [VbVbalrStrings#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#44)]  
  
 In diesem Beispiel führt die `Mid`\-Funktion eine direkte Operation an `aString` aus und weist dabei den Wert `bString` zu.  
  
 Eine Liste von Visual Basic\-Zeichenfolgenbearbeitungsmethoden finden Sie unter [String Manipulation Summary](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).  
  
### Freigegebene Methoden und Instanzmethoden  
 Sie können Zeichenfolgen auch mit den Methoden der `String`\-Klasse bearbeiten.  Es gibt zwei Methodentypen in `String`: *freigegebene* Methoden und *Instanz*methoden.  
  
#### Shared\-Methoden  
 Eine freigegebene Methode ist eine Methode, die von der `String`\-Klasse selbst abstammt und zur Ausführung keine Instanz dieser Klasse benötigt.  Diese Methoden können mit dem Namen der Klasse  \(`String`\) und nicht mit einer Instanz der `String`\-Klasse qualifiziert werden.  Beispiele:  
  
 [!CODE [VbVbalrStrings#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#45)]  
  
 Im oben stehenden Beispiel ist die <xref:System.String.Copy%2A?displayProperty=fullName>\-Methode eine statische Methode, die auf einen Ausdruck angewendet wird und `bString` den Ergebniswert zuweist.  
  
#### Instanzmethoden  
 Instanzmethoden stammen dagegen von einer bestimmten Instanz von `String` und müssen mit dem Instanznamen qualifiziert werden.  Beispiele:  
  
 [!CODE [VbVbalrStrings#46](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#46)]  
  
 In diesem Beispiel ist die <xref:System.String.Substring%2A?displayProperty=fullName>\-Methode eine Methode der Instanz von `String` \(d. h. von `aString`\).  Sie führt eine Operation an `aString` aus und weist `bString` den Wert zu.  
  
 Weitere Informationen finden Sie in der Dokumentation zur <xref:System.String>\-Klasse.  
  
## Siehe auch  
 [Introduction to Strings in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)