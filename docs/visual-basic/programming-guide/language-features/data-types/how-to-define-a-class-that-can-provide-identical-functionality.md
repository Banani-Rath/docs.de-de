---
title: "Gewusst wie: Definieren einer Klasse, die f&#252;r unterschiedliche Datentypen die gleiche Funktionalit&#228;t bereitstellen kann (Visual Basic) | Microsoft Docs"
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
  - "Datentypargumente, Verwenden"
  - "Typparameter, Definieren"
  - "Datentypargumente, Definieren"
  - "Argumente [Visual Basic], Datentypen"
  - "Of-Schlüsselwort, Verwenden"
  - "Einschränkungen, Generische Visual Basic-Typen"
  - "Generische Parameter"
  - "Datentypparameter"
  - "Datentypparameter, Verwenden"
  - "Generika [Visual Basic], Definieren von Klassen mit Typparametern"
  - "Datentypen [Visual Basic], Als Parameter"
  - "Datentypen [Visual Basic], Als Argumente"
  - "Parameter, Typ"
  - "Typargumente"
  - "Typen [Visual Basic], Generische"
  - "Parameter, Generische"
  - "Typparameter"
  - "Datentypargumente"
  - "Parameter, Datentyp"
  - "Generika [Visual Basic], Definieren von generischen Typen"
  - "Datentypparameter, Definieren"
  - "Typargumente, Definieren"
  - "Argumente [Visual Basic], Typ"
ms.assetid: a914adf8-e68f-4819-a6b1-200d1cf1c21c
caps.latest.revision: 29
caps.handback.revision: 29
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Gewusst wie: Definieren einer Klasse, die f&#252;r unterschiedliche Datentypen die gleiche Funktionalit&#228;t bereitstellen kann (Visual Basic)
Sie können eine Klasse definieren, über die Sie Objekte erstellen können, die für unterschiedliche Datentypen die gleiche Funktionalität bereitstellen. Hierzu geben Sie in der Definition mindestens einen *Typparameter* an. Die Klasse kann dann als Vorlage für Objekte fungieren, für die verschiedene Datentypen verwendet werden. Eine in dieser Weise definierte Klasse wird als *generische Klasse* bezeichnet.  
  
 Der Vorteil des Definierens einer generischen Klasse besteht darin, dass Sie die Klasse nur einmal definieren müssen und diese in Ihrem Code verwenden können, um viele Objekte zu erstellen, für die unterschiedliche Datentypen verwendet werden. Dies führt zu einer besseren Leistung, als dies der Fall ist, wenn die Klasse mit dem `Object`\-Typ definiert wird.  
  
 Zusätzlich zu generischen Klassen können Sie auch generische Strukturen, Schnittstellen, Prozeduren und Delegaten definieren und verwenden.  
  
### So definieren Sie eine Klasse mit einem Typparameter  
  
1.  Definieren Sie die Klasse auf die übliche Weise.  
  
2.  Fügen Sie `(Of` *Typparameter*`)` unmittelbar nach dem Klassennamen hinzu, um einen Typparameter anzugeben.  
  
3.  Sind mehrere Typparameter vorhanden, erstellen Sie innerhalb der Klammern eine Liste mit Kommas als Trennzeichen. Geben Sie das `Of`\-Schlüsselwort nur einmal an.  
  
4.  Werden im Code Operationen für einen Typparameter ausgeführt, die über eine einfache Zuweisung hinausgehen, geben Sie nach dem Typparameter eine `As`\-Klausel an, um die entsprechende Anzahl von *Einschränkungen* hinzuzufügen. Eine Einschränkung gewährleistet, dass der für den Typparameter angegebene Typ eine Anforderung erfüllt, beispielsweise eine der folgenden:  
  
    -   Unterstützt eine Operation, etwa `>`, die der Code ausführt  
  
    -   Unterstützt einen Member, etwa eine Methode, auf den der Code zugreift  
  
    -   Macht einen parameterlosen Konstruktor verfügbar  
  
     Wenn Sie keine Einschränkungen angeben, können im Code nur Operationen und Member verwendet werden, die vom [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) unterstützt werden. Weitere Informationen finden Sie unter [Type List](../../../../visual-basic/language-reference/statements/type-list.md).  
  
5.  Ermitteln Sie jeden Klassenmember, der mit einem bereitgestellten Typ deklariert werden muss, und deklarieren Sie ihn mit `As` `typeparameter`. Dies gilt für die interne Speicherung, für Prozedurparameter und für Rückgabewerte.  
  
6.  Im Code dürfen nur Operationen und Methoden verwenden, die von jedem Datentyp unterstützt werden, der im Code für `itemType` angegeben werden kann.  
  
     Im folgenden Beispiel wird eine Klasse definiert, in der eine sehr einfache Liste verwaltet wird. Die Klasse speichert die Liste im internen Array `items`, und der verwendende Code kann den Datentyp der Listenelemente deklarieren. Mit einem parametrisierten Konstruktor wird es dem verwendenden Code ermöglicht, die Obergrenze von `items` festzulegen, und der Standardkonstruktor legt diese auf 9 \(für insgesamt 10 Elemente\) fest.  
  
     [!CODE [VbVbalrDataTypes#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#7)]  
  
     Sie können eine Klasse aus `simpleList` deklarieren, die eine Liste von `Integer`\-Werten enthält, eine andere Klasse, die eine Liste von `String`\-Werten enthält, und eine weitere Klasse, die `Date`\-Werte enthält. Abgesehen vom Datentyp der Listenmember verhalten sich Objekte, die aus einer dieser Klassen erstellt wurden, gleich.  
  
     Das Typargument, das im verwendenden Code für `itemType` bereitgestellt wird, kann ein systeminterner Typ, etwa `Boolean` oder `Double`, eine Struktur, eine Enumeration oder ein beliebiger Klassentyp sein, einschließlich eines in der Anwendung definierten Klassentyps.  
  
     Sie können die Klasse `simpleList` mit dem folgenden Code testen.  
  
     [!CODE [VbVbalrDataTypes#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#8)]  
  
## Siehe auch  
 [Datentypen](../../../../visual-basic/programming-guide/language-features/data-types/index.md)   
 [Generische Typen in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Sprachenunabhängigkeit und sprachunabhängige Komponenten](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md)   
 [Of](../../../../visual-basic/language-reference/statements/of-clause.md)   
 [Type List](../../../../visual-basic/language-reference/statements/type-list.md)   
 [Gewusst wie: Verwenden einer generischen Klasse](../../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)   
 [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md)