---
title: "&#39;As Any&#39; is not supported in &#39;Declare&#39; statements | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30828"
  - "vbc30828"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30828"
ms.assetid: 7e5cf519-8b64-4ac5-8116-705fe26c846d
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;As Any&#39; is not supported in &#39;Declare&#39; statements
Der `Any`\-Datentyp wurde in Visual Basic 6.0 und früheren Versionen in `Declare`\-Anweisungen verwendet, um die Verwendung von Argumenten zu ermöglichen, die Daten eines beliebigen Typs enthalten konnten.  [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] unterstützt jedoch Überladen und löst so den `Any`\-Datentyp ab.  
  
 **Fehler\-ID:** BC30828  
  
### So beheben Sie diesen Fehler  
  
1.  Deklarieren Sie Parameter des jeweiligen Typs, den Sie verwenden möchten. Beispiel:  
  
     [!CODE [VbVbalrStatements#95](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#95)]  
  
2.  Verwenden Sie das <xref:System.Runtime.InteropServices.MarshalAsAttribute>\-Attribut, um `As Any` anzugeben, wenn von der aufgerufenen Prozedur `Void*` erwartet wird.  
  
     [!CODE [VbVbalrStatements#96](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#96)]  
  
## Siehe auch  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>   
 [Walkthrough: Calling Windows APIs](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)   
 [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md)   
 [Creating Prototypes in Managed Code](../Topic/Creating%20Prototypes%20in%20Managed%20Code.md)