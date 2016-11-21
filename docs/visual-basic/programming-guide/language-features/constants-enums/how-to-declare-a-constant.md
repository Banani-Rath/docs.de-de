---
title: "How to: Declare A Constant (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.constant"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Integer data type, declaring constants"
  - "Single data type, declaring constants"
  - "Const statement [Visual Basic], declaring constants"
  - "procedures, declaration"
  - "data types [Visual Basic], constants"
  - "Long data type, declaring constants"
  - "Visual Basic code, declaring variables and constants"
  - "Double data type, declaring constants"
  - "Boolean data type, declaring constants"
  - "modules, declaring constants"
  - "Byte data type, declaring constants"
  - "constants, declaring"
  - "Date data type, declaring constants"
  - "String data type, declaring constants"
  - "declaring constants, const keyword"
  - "Currency data type, declaring constants and variants"
  - "module-level constants and variables"
  - "Object data type, declaring constants"
ms.assetid: f901b4fa-481f-4621-822e-427060577ad1
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Declare A Constant (Visual Basic)
Mithilfe der `Const`\-Anweisung wird eine Konstante deklariert und ihr Wert festgelegt.  Durch Deklarieren einer Konstante weisen Sie einem Wert einen aussagekräftigen Namen zu.  Nachdem eine Konstante deklariert wurde, können Sie sie weder verändern noch ihr einen neuen Wert zuweisen.  
  
 Eine Konstante wird innerhalb einer Prozedur oder im Deklarationsabschnitt eines Moduls, einer Klasse oder Struktur deklariert.  Konstanten auf Klassen\- oder Strukturebene sind standardmäßig `Private`, können aber auch als `Public`, `Friend`, `Protected` oder `Protected Friend` deklariert werden, um die entsprechende Codezugriffsebene zu erhalten.  
  
 Die Konstante muss einen gültigen symbolischen Namen haben \(die Regeln für die Namenserstellung sind identisch mit denen für Variablennamen\) und der Konstantenausdruck muss aus numerischen oder Zeichenfolgenkonstanten und \-operatoren \(jedoch nicht aus Funktionsaufrufen\) zusammengesetzt sein.  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So deklarieren Sie eine Konstante  
  
-   Schreiben Sie eine Deklaration, die einen Zugriffsspezifizierer, das `Const`\-Schlüsselwort und einen Ausdruck enthält. Beispiel:  
  
     [!CODE [VbEnumsTask#8](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#8)]  
  
     Wenn [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) `Off` und [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) `On` ist, müssen Konstanten explizit durch Angabe eines Datentyps \(`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single` oder `String`\) deklariert werden.  
  
     Wenn `Option Infer` `On` oder `Option Strict` is `Off` ist, können Sie eine Konstante ohne Angabe eines Datentyps mit einer `As`\-Klausel deklarieren.  Der Compiler bestimmt den Typ der Konstante anhand des Ausdruckstyps.  Weitere Informationen finden Sie unter [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md).  
  
### So deklarieren Sie eine Konstante, die einen explizit angegebenen Datentyp besitzt  
  
-   Schreiben Sie eine Deklaration, die das `As`\-Schlüsselwort und einen expliziten Datentyp enthält \(siehe folgende Beispiele\):  
  
     [!CODE [VbEnumsTask#9](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#9)]  
  
     Sie können mehrere Konstanten in einer einzelnen Zeile deklarieren. Der Code ist jedoch besser lesbar, wenn Sie pro Zeile nur eine Konstante deklarieren.  Wenn Sie mehrere Konstanten auf einer Zeile deklarieren, müssen alle die gleiche Zugriffsebene aufweisen \(`Public`, `Private`, `Friend`, `Protected` oder `Protected Friend`\).  
  
### So deklarieren Sie mehrere Konstanten in einer Zeile  
  
-   Trennen Sie die Deklarationen mit einem Komma und einem Leerzeichen voneinander. Beispiel:  
  
    ```  
    Public Const Four As Integer = 4, Five As Integer = 5, Six As Integer = 44  
    ```  
  
## Siehe auch  
 [Const Statement](../../../../visual-basic/language-reference/statements/const-statement.md)   
 [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)   
 [Constants and Enumerations](../../../../visual-basic/programming-guide/language-features/constants-enums/index.md)   
 [Enumerations Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)   
 [Constants Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)   
 [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)   
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)   
 [Constants and Enumerations](../../../../visual-basic/language-reference/constants-and-enumerations.md)