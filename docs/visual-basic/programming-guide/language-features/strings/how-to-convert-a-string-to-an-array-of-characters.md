---
title: "How to: Convert a String to an Array of Characters in Visual Basic | Microsoft Docs"
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
  - "character arrays, converting strings"
  - "arrays [Visual Basic], converting strings to"
  - "examples [Visual Basic], string conversion"
  - "strings [Visual Basic], converting to arrays"
  - "string conversion [Visual Basic], arrays"
ms.assetid: 1b54b686-ab29-413b-adce-6bd5422376eb
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Convert a String to an Array of Characters in Visual Basic
Zuweilen empfiehlt es sich, Daten über die Zeichen in der Zeichenfolge und über deren Position in der Zeichenfolge zu erlangen, z. B. beim Analysieren einer Zeichenfolge.  In diesem Beispiel wird veranschaulicht, wie Sie ein Array von Zeichen in einer Zeichenfolge durch den Aufruf der <xref:System.String.ToCharArray%2A>\-Methode der Zeichenfolge abrufen.  
  
## Beispiel  
 In diesem Beispielen wird das Aufteilen einer Zeichenfolge in ein `Char`\-Array und das Aufteilen einer Zeichenfolge in ein `String`\-Array von Unicode\-Textzeichen veranschaulicht.  Diese Unterscheidung erfolgt, weil Unicode\-Textzeichen aus zwei oder mehr `Char`\-Zeichen \(z. B. einem Ersatzzeichenpaar oder einer Kombinationszeichenfolge\) bestehen können.  Weitere Informationen finden Sie unter <xref:System.Globalization.TextElementEnumerator> und in "The Unicode Standard" unter http:\/\/www.unicode.org.  
  
 [!CODE [VbVbalrStrings#75](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#75)]  
  
## Beispiel  
 Das Aufteilen einer Zeichenfolge in ihre Unicode\-Textzeichen ist schwieriger, doch erforderlich, wenn Sie Informationen über die visuelle Darstellung einer Zeichenfolge benötigen.  In diesem Beispiel wird die <xref:System.Globalization.StringInfo.SubstringByTextElements%2A>\-Methode zum Abrufen von Informationen über die Unicode\-Textzeichen verwendet, aus denen eine Zeichenfolge besteht.  
  
 [!CODE [VbVbalrStrings#76](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#76)]  
  
## Siehe auch  
 <xref:System.String.Chars%2A>   
 <xref:System.Globalization.StringInfo?displayProperty=fullName>   
 [How to: Access Characters in Strings](../../../../visual-basic/programming-guide/language-features/strings/how-to-access-characters-in-strings.md)   
 [Converting Between Strings and Other Data Types in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)   
 [Strings](../../../../visual-basic/programming-guide/language-features/strings/index.md)