---
title: "Gewusst wie: Verwenden einer generischen Klasse (Visual Basic) | Microsoft Docs"
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
  - "Typparameter, Definieren"
  - "Datentypargumente, Definieren"
  - "Argumente [Visual Basic], Datentypen"
  - "Of-Schlüsselwort, Verwenden"
  - "Generische Parameter"
  - "Datentypparameter"
  - "Generika [Visual Basic], Informationen über Generika"
  - "Datentypen [Visual Basic], Als Parameter"
  - "Datentypen [Visual Basic], Als Argumente"
  - "Parameter, Typ"
  - "Typen [Visual Basic], Generische"
  - "Parameter, Generische"
  - "Generika [Visual Basic], Erstellen generischer Typen"
  - "Datentypargumente"
  - "Parameter, Datentyp"
  - "Datentypparameter, Definieren"
  - "Typargumente, Definieren"
  - "Argumente [Visual Basic], Typ"
ms.assetid: 242dd2a6-86c4-4ce7-83f2-f2661803f752
caps.latest.revision: 24
caps.handback.revision: 24
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Gewusst wie: Verwenden einer generischen Klasse (Visual Basic)
Eine Klasse, die *Typparameter* akzeptiert, wird *generische Klasse* genannt. Wenn Sie eine generische Klasse verwenden, können Sie daraus eine *erzeugte Klasse* generieren, indem Sie ein *Typargument* für jeden dieser Parameter angeben. Sie können dann eine Variable vom Typ der erzeugten Klasse deklarieren, und Sie können eine Instanz der erzeugten Klasse erstellen und dieser Variablen zuweisen.  
  
 Zusätzlich zu generischen Klassen können Sie auch generische Strukturen, Schnittstellen, Prozeduren und Delegaten definieren und verwenden.  
  
 Beim folgenden Verfahren wird eine generische Klasse verwendet, die in [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] definiert ist, und eine Instanz daraus erstellt.  
  
### Eine Klasse verwenden, die einen Typparameter braucht  
  
1.  Fügen Sie am Anfang der Quelldatei ein [Imports Statement \(.NET Namespace and Type\)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) zum Importieren des <xref:System.Collections.Generic?displayProperty=fullName> Namespace hinzu. Dadurch können Sie auf die <xref:System.Collections.Generic.Queue%601?displayProperty=fullName>\-Klasse verweisen, ohne sie zur Unterscheidung von anderen Warteschlangenklassen wie z.B. <xref:System.Collections.Queue?displayProperty=fullName> vollständig qualifizieren zu müssen.  
  
2.  Erstellen Sie das Objekt auf die übliche Weise, aber fügen Sie sofort nach dem Klassennamen `(Of` `type``)` hinzu.  
  
     Im folgenden Beispiel wird dieselbe Klasse \(<xref:System.Collections.Generic.Queue%601?displayProperty=fullName>\) verwendet, um zwei Warteschlangenobjekte zu erstellen, die Artikel mit unterschiedlichen Datentypen enthalten. Es fügt Elemente am Ende jeder Warteschlange ein und entfernt und zeigt Elemente am Beginn jeder Warteschlange.  
  
     [!CODE [VbVbalrDataTypes#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#9)]  
  
## Siehe auch  
 [Datentypen](../../../../visual-basic/programming-guide/language-features/data-types/index.md)   
 [Generische Typen in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Sprachenunabhängigkeit und sprachunabhängige Komponenten](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md)   
 [Of](../../../../visual-basic/language-reference/statements/of-clause.md)   
 [Imports Statement \(.NET Namespace and Type\)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)   
 [Gewusst wie: Definieren einer Klasse, die für unterschiedliche Datentypen die gleiche Funktionalität bereitstellen kann](../../../../visual-basic/programming-guide/language-features/data-types/how-to-define-a-class-that-can-provide-identical-functionality.md)   
 [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)