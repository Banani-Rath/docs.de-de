---
title: "How to: Convert an Array of Bytes into a String in Visual Basic | Microsoft Docs"
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
  - "byte arrays, converting to strings"
  - "examples [Visual Basic], strings"
  - "arrays [Visual Basic], converting to strings"
ms.assetid: d0dc8317-9ab3-4324-99f7-3f5788c0e72a
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Convert an Array of Bytes into a String in Visual Basic
Dieses Thema zeigt, wie die Bytes eines Bytearrays in eine Zeichenfolge konvertiert werden.  
  
## Beispiel  
 Im folgenden Beispiel werden mit der <xref:System.Text.Encoding.GetString%2A>\-Methode der <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName>\-Codierungsklasse alle Bytes eines Bytearrays in eine Zeichenfolge konvertiert.  
  
 [!CODE [VbVbalrStrings#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#72)]  
  
 Sie können unter mehreren Codierungsoptionen wählen, wenn Sie ein Bytearray in eine Zeichenfolge konvertieren möchten:  
  
-   <xref:System.Text.Encoding.ASCII%2A?displayProperty=fullName>: Ruft eine Codierung für den ASCII\-Zeichensatz \(7 Bits\) ab.  
  
-   <xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-16\-Format mit Big\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.Default%2A?displayProperty=fullName>: Ruft eine Codierung für die aktuelle ANSI\-Codepage des Systems ab.  
  
-   <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-16\-Format mit Little\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.UTF32%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-32\-Format mit Little\-Endian\-Bytereihenfolge ab.  
  
-   <xref:System.Text.Encoding.UTF7%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-7\-Format ab.  
  
-   <xref:System.Text.Encoding.UTF8%2A?displayProperty=fullName>: Ruft eine Codierung für das UTF\-8\-Format ab.  
  
## Siehe auch  
 <xref:System.Text.Encoding?displayProperty=fullName>   
 <xref:System.Text.Encoding.GetString%2A>   
 [How to: Convert Strings into an Array of Bytes in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-strings-into-an-array-of-bytes.md)