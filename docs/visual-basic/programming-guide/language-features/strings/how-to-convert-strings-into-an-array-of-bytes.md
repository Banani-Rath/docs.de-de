---
title: "How to: Convert Strings into an Array of Bytes in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "string conversion, arrays"
  - "arrays [Visual Basic], converting strings to"
  - "byte arrays"
  - "examples [Visual Basic], string conversion"
  - "arrays [Visual Basic], byte arrays"
ms.assetid: f477d35c-a3fc-4a30-b1d4-cd0d353aae1d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Convert Strings into an Array of Bytes in Visual Basic
In diesem Thema wird dargestellt, wie eine Zeichenfolge in ein Bytearray konvertiert wird.  
  
## Beispiel  
 Im folgenden Beispiel wird die <xref:System.Text.Encoding.GetBytes%2A>\-Methode der <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName>\-Codierungsklasse verwendet, um eine Zeichenfolge in ein Bytearray zu konvertieren.  
  
 [!CODE [VbVbalrStrings#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#74)]  
  
 Sie können unter mehreren Codierungsoptionen wählen, um eine Zeichenfolge in ein Bytearray zu konvertieren:  
  
-   <xref:System.Text.Encoding.ASCII%2A?displayProperty=fullName>: Ruft eine Codierung für den ASCII\-Zeichensatz \(7 Bits\) ab.  
  
-   <xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-16\-Format mit Big\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.Default%2A?displayProperty=fullName>: Ruft eine Codierung für die aktuelle ANSI\-Codepage des Systems ab.  
  
-   <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-16\-Format mit Little\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.UTF32%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-32\-Format mit Little\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.UTF7%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-7\-Format ab.  
  
-   <xref:System.Text.Encoding.UTF8%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-8\-Format ab.  
  
## Siehe auch  
 <xref:System.Text.Encoding?displayProperty=fullName>   
 <xref:System.Text.Encoding.GetBytes%2A>   
 [How to: Convert an Array of Bytes into a String in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-an-array-of-bytes-into-a-string.md)