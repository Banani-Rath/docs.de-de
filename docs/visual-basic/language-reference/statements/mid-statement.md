---
title: "Mid Statement | Microsoft Docs"
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
  - "vb.MidB"
  - "vb.Mid"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "substrings, Mid statement"
  - "strings [Visual Basic], substrings"
  - "Mid statement"
  - "strings [Visual Basic], replacing"
ms.assetid: 2b82d7a8-9646-4cb0-bec5-80abc98297bf
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Mid Statement
Ersetzt eine bestimmte Anzahl an Zeichen in einer `String`\-Variablen durch Zeichen aus einer anderen Zeichenfolge.  
  
## Syntax  
  
```  
Mid( _  
   ByRef Target As String, _  
   ByVal Start As Integer, _  
   Optional ByVal Length As Integer _  
) = StringExpression  
```  
  
## Teile  
 `Target`  
 Erforderlich.  Name der zu ändernden `String`\-Variablen.  
  
 `Start`  
 Erforderlich.  `Integer`\-Ausdruck.  Die Zeichenposition in `Target`, wo die Ersetzung von Text beginnt.  `Start` verwendet einen auf Eins basierten Index.  
  
 `Length`  
 Optional.  `Integer`\-Ausdruck.  Anzahl der zu ersetzenden Zeichen.  Wird hierfür kein Wert angegeben, so wird `String` komplett verwendet.  
  
 `StringExpression`  
 Erforderlich.  `String`\-Ausdruck, der einen Teil von `Target` ersetzt.  
  
## Ausnahmen  
  
|Ausnahmetyp|Bedingung|  
|-----------------|---------------|  
|<xref:System.ArgumentException>|`Start` \<\= 0 oder `Length` \< 0.|  
  
## Hinweise  
 Die Anzahl der ersetzten Zeichen ist immer kleiner oder gleich der Anzahl der Zeichen in `Target`.  
  
 Visual Basic verfügt über eine <xref:Microsoft.VisualBasic.Strings.Mid%2A>\-Funktion und eine `Mid`\-Anweisung.  Mit beiden Elementen wird eine angegebene Anzahl von Zeichen in einer Zeichenfolge bearbeitet. Die `Mid`\-Funktion gibt die Zeichen jedoch zurück, während die `Mid`\-Anweisung die Zeichen ersetzt.  Weitere Informationen finden Sie unter <xref:Microsoft.VisualBasic.Strings.Mid%2A>.  
  
> [!NOTE]
>  Die `MidB`\-Anweisung aus früheren Versionen von Visual Basic ersetzt eine Teilzeichenfolge in Bytes und nicht in Zeichen.  Sie wird primär zum Konvertieren von Zeichenfolgen in DBCS \(Double\-Byte Character Set\)\-Anwendungen verwendet.  Alle Visual Basic\-Zeichenfolgen sind im Unicode\-Format geschrieben. `MidB` wird nicht mehr unterstützt.  
  
## Beispiel  
 In diesem Beispiel wird der `Mid`\-Ausdruck verwendet, um eine bestimmte Anzahl von Zeichen in einer Zeichenfolgenvariablen durch Zeichen aus einer anderen Zeichenfolge zu ersetzen.  
  
 [!CODE [VbVbalrStrings#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#5)]  
  
## Anforderungen  
 **Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Modul:** `Strings`  
  
 **Assembly:** [!INCLUDE[vbprvbruntime](../../../visual-basic/language-reference/objects/includes/vbprvbruntime_md.md)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Strings.Mid%2A>   
 [Strings](../../../visual-basic/programming-guide/language-features/strings/index.md)   
 [Introduction to Strings in Visual Basic](../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)