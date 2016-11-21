---
title: "Character Data Types (Visual Basic) | Microsoft Docs"
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
  - "data types [Visual Basic], character"
  - "String data type, character data types"
  - "character data types [Visual Basic]"
  - "Char data type, character data types"
  - "data types [Visual Basic], choosing"
ms.assetid: 902479ef-1679-47fc-9911-0c1c5008226c
caps.latest.revision: 23
caps.handback.revision: 23
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Character Data Types (Visual Basic)
[!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] stellt *Zeichendatentypen* für die Verarbeitung von Zeichen, die gedruckt und angezeigt werden können, zur Verfügung.  Beide Zeichendatentypen verarbeiten Unicode\-Zeichen. `Char` enthält jedoch ein einzelnes Zeichen, `String` dagegen eine unbestimmte Anzahl von Zeichen.  
  
 Eine Tabelle mit einer Gegenüberstellung der [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Datentypen finden Sie unter [Data Types](../../../../visual-basic/language-reference/data-types/data-type-summary.md).  
  
## Char\-Typ  
 Der Datentyp `Char` ist ein einzelnes 2\-Byte\-\(16\-Bit\-\)Unicode\-Zeichen.  Wenn eine Variable immer genau ein Zeichen speichert, deklarieren Sie sie als `Char`.  Beispiele:  
  
 [!CODE [VbVbalrCharTypes#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrchartypes#1)]  
  
 Jeder mögliche Wert einer Variablen vom Typ `Char` oder `String` ist ein *Codepunkt* \(oder Zeichencode\) im Unicode\-Zeichensatz.  Der Unicode\-Zeichensatz umfasst den grundlegenden ASCII\-Zeichensatz, verschiedene andere Buchstaben, Akzente, Währungssymbole, Bruchzahlen, diakritische Zeichen sowie mathematische und technische Symbole.  
  
> [!NOTE]
>  Im Unicode\-Zeichensatz sind die Codepunkte D800 bis DFFF \(55296 bis 55551 in Dezimalschreibweise\) für *Ersatzpaare* reserviert, bei denen zwei 16\-Bit\-Werte zur Darstellung eines Codepunkts erforderlich sind.  In `Char`\-Variablen können keine Ersatzpaare abgelegt werden. In `String`\-Variablen sind für das Ablegen eines Ersatzpaares zwei Positionen erforderlich.  
  
 Weitere Informationen finden Sie unter [Char Data Type](../../../../visual-basic/language-reference/data-types/char-data-type.md).  
  
## String\-Typ  
 Der Datentyp `String` ist eine Folge von null oder mehr 2\-Byte\-\(16\-Bit\-\)Unicode\-Zeichen.  Wenn eine Variable eine unbestimmte Anzahl von Zeichen enthalten kann, deklarieren Sie sie als `String`.  Beispiele:  
  
 [!CODE [VbVbalrCharTypes#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrchartypes#2)]  
  
 Weitere Informationen finden Sie unter [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md).  
  
## Siehe auch  
 [Elementary Data Types](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)   
 [Composite Data Types](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)   
 [Generische Typen in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)   
 [Type Conversions in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)   
 [Troubleshooting Data Types](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)   
 [Type Characters](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)