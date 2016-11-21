---
title: "Key (Visual Basic) | Microsoft Docs"
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
  - "vb.AnonymousKey"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "anonymous types [Visual Basic], key"
  - "Key [Visual Basic]"
  - "Key keyword [Visual Basic]"
ms.assetid: 7697a928-7d14-4430-a72a-c9e96e8d6c11
caps.latest.revision: 22
caps.handback.revision: 22
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Key (Visual Basic)
Mit dem `Key`\-Schlüsselwort kann das Verhalten von Eigenschaften anonymer Typen festgelegt werden.  In Gleichheitstests zwischen Instanzen anonymen Typs und bei der Berechnung von Hashcodewerten werden nur als Haupteigenschaften deklarierte Eigenschaften einbezogen.  Die Werte von Haupteigenschaften können nicht geändert werden.  
  
 Eine Eigenschaft eines anonymen Typs wird als Haupteigenschaft gekennzeichnet, indem der Deklaration in der Initialisierungsliste das Schlüsselwort `Key` vorangestellt wird.  Im folgenden Beispiel sind `Airline` und `FlightNo` Haupteigenschaften, `Gate` jedoch nicht.  
  
 [!CODE [VbVbalrAnonymousTypes#26](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#26)]  
  
 Wenn ein neuer anonymer Typ erstellt wird, erbt er direkt von <xref:System.Object>.  Der Compiler überschreibt drei geerbte Member: <xref:System.Object.Equals%2A>, <xref:System.Object.GetHashCode%2A> und <xref:System.Object.ToString%2A>.  Der Überschreibungscode, der für <xref:System.Object.Equals%2A> erzeugt wird, und <xref:System.Object.GetHashCode%2A> basieren auf Haupteigenschaften.  Wenn der betreffende Typ keine Haupteigenschaften hat, werden <xref:System.Object.GetHashCode%2A> und <xref:System.Object.Equals%2A> nicht überschrieben.  
  
## Gleichheit  
 Zwei Instanzen eines anonymen Typs sind gleich, wenn sie Instanzen desselben Typs sind und die Werte ihrer Haupteigenschaften übereinstimmen.  In folgenden Beispielen stimmt `flight2` mit `flight1` aus dem vorigen Beispiel überein, da sie Instanzen vom gleichen anonymen Typ sind und die gleichen Werte für ihre Haupteigenschaften haben.  `flight3` entspricht allerdings nicht `flight1`, da der Wert einer Haupteigenschaft abweicht: `FlightNo`.  Die Instanz `flight4` ist nicht der gleiche Typ wie `flight1`, da sie andere Eigenschaften als Haupteigenschaften festlegen.  
  
 [!CODE [VbVbalrAnonymousTypes#27](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#27)]  
  
 Wenn zwei Instanzen ohne Haupteigenschaften deklariert werden, sind sie auch dann nicht gleich, wenn Name, Typ, Reihenfolge und Wert übereinstimmen.  Eine Instanz ohne Haupteigenschaften gleicht nur sich selbst.  
  
 Weitere Informationen zu den Bedingungen, unter denen zwei Instanzen anonymen Typs Instanzen des gleichen anonymen Typs sind, finden Sie unter [Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
  
## Hashcodeberechnung  
 Wie <xref:System.Object.Equals%2A> basiert auch die unter <xref:System.Object.GetHashCode%2A> definierte Hashfunktion für einen anonymen Typ auf den Haupteigenschaften des Typs.  In den folgenden Beispielen wird die Interaktion zwischen Haupteigenschaften und Hashcodewerten veranschaulicht.  
  
 Instanzen eines anonymen Typs mit dem gleichen Wert für alle Haupteigenschaften verfügen auch dann über den gleichen Hashcodewert, wenn die Werte der Nicht\-Haupteigenschaften nicht übereinstimmen.  Die folgende Anweisung gibt `True` zurück.  
  
 [!CODE [VbVbalrAnonymousTypes#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#37)]  
  
 Instanzen eines anonymen Typs mit unterschiedlichen Werten für mindestens eine Haupteigenschaft verfügen über unterschiedliche Hashcodewerte.  Die folgende Anweisung gibt `False` zurück.  
  
 [!CODE [VbVbalrAnonymousTypes#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#38)]  
  
 Instanzen anonymen Typs, die unterschiedliche Eigenschaften als Haupteigenschaften festlegen, sind keine Instanzen des gleichen Typs.  Sie verfügen auch dann über verschiedene Hashcodewerte, wenn die Namen und Werte aller Eigenschaften gleich sind.  Die folgende Anweisung gibt `False` zurück.  
  
 [!CODE [VbVbalrAnonymousTypes#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#39)]  
  
## Schreibgeschützte Werte  
 Die Werte von Haupteigenschaften können nicht geändert werden.  In `flight1` aus obigen Beispielen sind die Felder `Airline` und `FlightNo` beispielsweise schreibgeschützt, das Feld `Gate` kann jedoch geändert werden.  
  
 [!CODE [VbVbalrAnonymousTypes#28](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrAnonymousTypes#28)]  
  
## Siehe auch  
 [Anonymous Type Definition](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-type-definition.md)   
 [Gewusst wie: Ableiten von Eigenschaftennamen und Typen in Deklarationen von anonymen Typen](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)   
 [Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)