---
title: "How to: Access Characters in Strings in Visual Basic | Microsoft Docs"
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
  - "strings [Visual Basic], accessing characters"
  - "characters [Visual Basic], accessing in strings"
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Access Characters in Strings in Visual Basic
In diesem Beispiel wird die Verwendung der <xref:System.String.Chars%2A>\-Eigenschaft für den Zugriff auf das Zeichen an einer angegebenen Position in einer Zeichenfolge veranschaulicht.  
  
## Beispiel  
 Zuweilen empfiehlt es sich, Daten über die Zeichen in der Zeichenfolge und über deren Position in der Zeichenfolge zu erlangen.  Sie können sich eine Zeichenfolge als ein Array von Zeichen \(`Char`\-Instanzen\) vorstellen. Sie können ein bestimmtes Zeichen abrufen, indem Sie mithilfe der <xref:System.String.Chars%2A>\-Eigenschaft auf den Index des Zeichens verweisen.  
  
 [!CODE [VbVbalrStrings#49](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#49)]  
  
 Der `index`\-Parameter der <xref:System.String.Chars%2A>\-Eigenschaft ist nullbasiert.  
  
## Robuste Programmierung  
 Die <xref:System.String.Chars%2A>\-Eigenschaft gibt das Zeichen an der angegebenen Position zurück.  Einige Unicode\-Zeichen können jedoch durch mehrere Zeichen dargestellt werden.  Weitere Informationen über das Arbeiten mit Unicode\-Zeichen finden Sie unter [How to: Convert a String to an Array of Characters](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).  
  
 Die <xref:System.String.Chars%2A>\-Eigenschaft löst eine <xref:System.IndexOutOfRangeException>\-Ausnahme aus, wenn der `index`\-Parameter größer oder gleich der Zeichenfolgenlänge oder kleiner als 0 \(null\) ist.  
  
## Siehe auch  
 <xref:System.String.Chars%2A>   
 [How to: Convert a String to an Array of Characters](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)   
 [Converting Between Strings and Other Data Types in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)   
 [Strings](../../../../visual-basic/programming-guide/language-features/strings/index.md)