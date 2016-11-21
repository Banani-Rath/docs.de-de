---
title: "How to: Group Related Constant Values Together (Visual Basic) | Microsoft Docs"
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
  - "enumerations [Visual Basic], constants"
  - "constants, grouping together"
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Group Related Constant Values Together (Visual Basic)
Verwandte Konstanten lassen sich am besten mit Enumerationen gruppieren.  Sie können eine Enumeration mithilfe der `Enum`\-Anweisung im Deklarationsabschnitt einer Klasse oder eines Moduls erstellen.  Weitere Informationen finden Sie unter [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).  
  
### So gruppieren Sie verwandte konstante Werte  
  
1.  Schreiben Sie eine Deklaration mit einer Codezugriffsebene, dem `Enum`\-Schlüsselwort und einem gültigen Namen.  In diesem Beispiel wird die `Private`\-Enumeration `temperatureValues` erstellt.  
  
     [!CODE [VbEnumsTask#21](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#21)]  
  
2.  Definieren Sie die Konstanten der Enumeration.  In diesem Beispiel werden die `Public`\-Enumeration `temperatureValues` erstellt und die entsprechenden Werte zugewiesen.  
  
     [!CODE [VbEnumsTask#1](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#1)]  
  
## Siehe auch  
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [How to: Refer to an Enumeration Member](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)   
 [When to Use an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)   
 [Constants Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)   
 [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)   
 [Constants and Enumerations](../../../../visual-basic/language-reference/constants-and-enumerations.md)