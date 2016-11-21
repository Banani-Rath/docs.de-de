---
title: "User-Defined Constants (Visual Basic) | Microsoft Docs"
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
  - "constants, circular references"
  - "Const statement [Visual Basic], user-defined constants"
  - "user-defined constants"
  - "scope, constants"
  - "constants, user-defined"
  - "circular references between constants"
ms.assetid: a1206d5c-c45e-4ac2-970a-4a0be6a05fdd
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# User-Defined Constants (Visual Basic)
Eine Konstante ist ein aussagekräftiger Name, der anstelle einer unveränderlichen Zahl oder Zeichenfolge verwendet wird.  Konstanten speichern Werte, die \(wie der Name sagt\) während der Ausführung einer Anwendung konstant bleiben.  Sie können Konstanten verwenden, die in den von Ihnen verwendeten Steuerelementen oder Komponenten definiert sind, oder selbst Konstanten erstellen.  Vom Benutzer selbst erstellte Konstanten werden auch als *benutzerdefiniert* bezeichnet.  
  
 Zum Deklarieren von Konstanten verwenden Sie die `Const`\-Anweisung, wobei dieselben Richtlinien wie bei der Erstellung eines Variablennamens gelten.  Wenn `Option Strict` den Wert `On` hat, müssen Sie den Konstantentyp explizit deklarieren.  
  
## Verwenden der Const\-Anweisung  
 Eine `Const`\-Anweisung stellt eine mathematische oder Datums\-\/Uhrzeitmenge dar:  
  
 [!CODE [VbEnumsTask#10](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#10)]  
  
 Es können auch `String`\-Konstanten definiert werden:  
  
 [!CODE [VbEnumsTask#13](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#13)]  
  
 Der Ausdruck auf der rechten Seite des Gleichheitszeichens \(`=`\) ist häufig eine Zahl oder Literalzeichenfolge. Es kann sich jedoch auch um einen Ausdruck handeln, der eine Zahl oder Zeichenfolge ergibt \(obwohl ein solcher Ausdruck keine Funktionsaufrufe enthalten darf\).  Sie können sogar Konstanten basierend auf zuvor definierten Konstanten definieren:  
  
 [!CODE [VbEnumsTask#15](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#15)]  
  
## Gültigkeitsbereich von benutzerdefinierten Konstanten  
 Der Gültigkeitsbereich einer `Const`\-Konstante entspricht dem einer an derselben Position deklarierten Variablen.  Sie haben folgende Möglichkeiten zum Festlegen des Gültigkeitsbereichs:  
  
-   Wenn Sie eine Konstante erstellen möchten, die nur innerhalb einer Prozedur vorhanden ist, deklarieren Sie die Konstante innerhalb dieser Prozedur.  
  
-   Wenn Sie eine Konstante erstellen möchten, die für alle Prozeduren in einer Klasse, nicht jedoch für Code außerhalb des Moduls verfügbar ist, deklarieren Sie sie im Deklarationsabschnitt der Klasse.  
  
-   Wenn Sie eine Konstante erstellen möchten, die für alle Member einer Assembly, nicht jedoch für Clients außerhalb der Assembly verfügbar ist, deklarieren Sie sie mithilfe des `Friend`\-Schlüsselworts im Deklarationsabschnitt der Klasse.  
  
-   Wenn Sie eine Konstante erstellen möchten, die innerhalb der gesamten Anwendung verfügbar ist, deklarieren Sie sie mithilfe des `Public`\-Schlüsselworts im Deklarationsabschnitt der Klasse.  
  
 Weitere Informationen finden Sie unter [How to: Declare A Constant](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md).  
  
### Vermeiden von zirkulären Verweisen  
 Da Konstanten mithilfe anderer Konstanten definiert werden können, kann es vorkommen, dass sich unbeabsichtigter Weise ein *zirkulärer Verweis* zwischen zwei oder mehr Konstanten ergibt.  Ein zirkulärer Verweis entsteht, wenn zwei oder mehr öffentliche Konstanten vorhanden sind, von denen jeweils die eine mithilfe der anderen definiert wurde. Beispiel:  
  
 [!CODE [VbEnumsTask#16](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#16)]  
[!CODE [VbEnumsTask#17](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#17)]  
  
 Im Fall eines zirkulären Verweises generiert [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] einen Compilerfehler.  
  
## Siehe auch  
 [Const Statement](../../../../visual-basic/language-reference/statements/const-statement.md)   
 [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)   
 [Constants and Enumerations](../../../../visual-basic/programming-guide/language-features/constants-enums/index.md)   
 [Constants and Enumerations](../../../../visual-basic/language-reference/constants-and-enumerations.md)   
 [Enumerations Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)   
 [Constants Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)   
 [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)   
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)