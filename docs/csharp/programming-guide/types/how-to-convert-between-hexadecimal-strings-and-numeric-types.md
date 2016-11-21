---
title: "Gewusst wie: Konvertieren zwischen Hexadezimalzeichenfolgen und numerischen Typen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Konvertierungen [C#], Hexadezimalzeichenfolgen"
  - "Hexadezimalzeichenfolgen [C#]"
  - "Hexadezimalzeichenfolgen [C#], Konvertieren in numerischen Typ"
  - "Zeichenfolgen [C#], Konvertieren von Hexadezimalzeichenfolgen"
ms.assetid: 7115c49f-7d1d-40c3-8bd9-aae0cc1d46b6
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Konvertieren zwischen Hexadezimalzeichenfolgen und numerischen Typen (C#-Programmierhandbuch)
In diesen Beispielen wird Ihnen gezeigt, wie die folgenden Aufgaben ausgeführt werden:  
  
-   Abrufen eines Hexadezimalwerts eines Zeichens in einer [Zeichenfolge](../../../csharp/language-reference/keywords/string.md).  
  
-   Abrufen von [char](../../../csharp/language-reference/keywords/char.md), das den einzelnen Werten in einer Hexadezimalzeichenfolge entspricht.  
  
-   Konvertieren eines hexadezimalen `string`\-Werts in eine Ganzzahl \([int](../../../csharp/language-reference/keywords/int.md)\).  
  
-   Konvertieren eines hexadezimalen `string`\-Werts in [float](../../../csharp/language-reference/keywords/float.md)\-Wert.  
  
-   Konvertieren eines Bytearrays \([byte](../../../csharp/language-reference/keywords/byte.md)\) in eine hexadezimale Zeichenfolge \(`string`\).  
  
## Beispiel  
 In diesem Beispiel wird der Hexadezimalwert jedes Zeichens in einer Zeichenfolge \(`string`\) ausgegeben.  Zunächst wird die Zeichenfolge \(`string`\) in ein Zeichenarray ausgewertet.  Anschließend wird für jedes Zeichen <xref:System.Convert.ToInt32%28System.Char%29> aufgerufen, um den numerischen Wert zu erhalten.  Zum Schluss wird die Zahl als Hexadezimaldarstellung in einer Zeichenfolge \(`string`\) formatiert.  
  
 [!CODE [csProgGuideTypes#30](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#30)]  
  
## Beispiel  
 In diesem Beispiel wird eine Zeichenfolge \(`string`\) von Hexadezimalwerten analysiert, und die den einzelnen Hexadezimalwerten entsprechenden Zeichen werden ausgegeben.  Zunächst wird die [Split\(Char\[\]\)](assetId:///M:System.String.Split(System.Char[])?qualifyHint=False&autoUpgrade=False)\-Methode aufgerufen, um die einzelnen Hexadezimalwerte als einzelne `string`\-Werte in einem Array zu erhalten.  Dann wird der Hexadezimalwert durch Aufrufen von <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29> in einen Dezimalwert konvertiert, der als Ganzzahlwert \([int](../../../csharp/language-reference/keywords/int.md)\) dargestellt wird.  Das Beispiel zeigt zwei verschiedene Möglichkeiten, das Zeichen zu erhalten, das diesem Zeichencode entspricht.  Bei der ersten Methode wird <xref:System.Char.ConvertFromUtf32%28System.Int32%29> verwendet, das das Zeichen, das dem ganzzahligen Argument entspricht, als `string`\-Zeichenfolge zurückgibt.  Bei der zweiten Möglichkeit wird der `int`\-Wert explizit in einen [char](../../../csharp/language-reference/keywords/char.md)\-Wert umgewandelt.  
  
 [!CODE [csProgGuideTypes#31](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#31)]  
  
## Beispiel  
 Dieses Beispiel zeigt eine weitere Möglichkeit zur Konvertierung einer Hexadezimalzeichenfolge \(`string`\) in einen Ganzzahlwert durch Aufrufen der <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29>\-Methode.  
  
 [!CODE [csProgGuideTypes#32](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#32)]  
  
## Beispiel  
 Im folgenden Beispiel wird dargestellt, wie eine Hexadezimalzeichenfolge \(`string`\) in einen [float](../../../csharp/language-reference/keywords/float.md)\-Wert konvertiert wird. Dazu werden die <xref:System.BitConverter?displayProperty=fullName>\-Klasse und die <xref:System.Int32.Parse%2A?displayProperty=fullName>\-Methode verwendet.  
  
 [!CODE [csProgGuideTypes#39](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#39)]  
  
## Beispiel  
 Im folgenden Beispiel wird dargestellt, wie ein Bytearray \([byte](../../../csharp/language-reference/keywords/byte.md)\) mithilfe der <xref:System.BitConverter?displayProperty=fullName>\-Klasse in eine Hexadezimalzeichenfolge konvertiert wird.  
  
 [!CODE [csProgGuideTypes#38](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#38)]  
  
## Siehe auch  
 [Standardmäßige Zahlenformatzeichenfolgen](../Topic/Standard%20Numeric%20Format%20Strings.md)   
 [Typen](../../../csharp/programming-guide/types/index.md)   
 [Gewusst wie: Bestimmen, ob eine Zeichenfolge einen numerischen Wert darstellt](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)