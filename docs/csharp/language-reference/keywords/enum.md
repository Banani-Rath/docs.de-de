---
title: "enum (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "enum"
  - "enum_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "enum-Schlüsselwort [C#]"
ms.assetid: bbeb9a0f-e9b3-41ab-b0a6-c41b1a08974c
caps.latest.revision: 36
caps.handback.revision: 36
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# enum (C#-Referenz)
Das Schlüsselwort `enum` wird zum Deklarieren einer Enumeration verwendet. Dies ist ein eigener Typ, der aus einer Gruppe benannter Konstanten besteht, die Enumeratorliste genannt wird.  
  
 In der Regel ist es am besten, eine Enumeration direkt innerhalb eines Namespaces so zu definieren, dass alle Klassen im Namespace auf gleiche Weise darauf zugreifen können. Eine Enumeration kann aber auch innerhalb einer Klasse oder einer Struktur geschachtelt werden.  
  
 Der erste Enumerator hat standardmäßig den Wert 0. Der Wert jedes nachfolgenden Enumerators wird um 1 erhöht. In der folgenden Enumeration gilt z. B.: `Sat` ist `0`, `Sun` ist `1`, `Mon` ist `2` usw.  
  
```  
  
enum Days {Sat, Sun, Mon, Tue, Wed, Thu, Fri};  
```  
  
 Enumeratoren können mithilfe von Initialisierern die Standardwerte überschreiben, wie im folgenden Beispiel gezeigt.  
  
```  
  
enum Days {Sat=1, Sun, Mon, Tue, Wed, Thu, Fri};  
```  
  
 In dieser Enumeration wird erzwungen, dass die Abfolge von Elementen mit `1` und nicht mit `0` beginnt. Allerdings wird das Einfügen einer Konstanten mit dem Wert 0 empfohlen. Weitere Informationen finden Sie unter [Enumerationstypen](../../../csharp/programming-guide/enumeration-types.md).  
  
 Jeder Enumerationstyp hat einen zugrunde liegenden Typ, bei dem es sich um jeden ganzzahligen Typ außer [char](../../../csharp/language-reference/keywords/char.md) handeln kann. Der zugrunde liegende Standardtyp von Enumerationselementen ist [int](../../../csharp/language-reference/keywords/int.md). Um eine Enumeration eines anderen ganzzahligen Typs, z. B. [byte](../../../csharp/language-reference/keywords/byte.md) zu deklarieren, setzen Sie einen Doppelpunkt hinter dem Bezeichner, auf den der Typ folgt, wie im folgenden Beispiel gezeigt.  
  
```  
  
enum Days : byte {Sat=1, Sun, Mon, Tue, Wed, Thu, Fri};  
```  
  
 Die zulässigen Typen für eine Enumeration sind `byte`, [sbyte](../../../csharp/language-reference/keywords/sbyte.md), [short](../../../csharp/language-reference/keywords/short.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) und [ulong](../../../csharp/language-reference/keywords/ulong.md).  
  
 Einer Variablen des Typs `Days` kann jeder Wert im Werbebereich des zugrunde liegenden Typs zugewiesen werden. Die Werte sind nicht auf benannte Konstanten beschränkt.  
  
 Der Standardwert von `enum E` ist der Wert, der vom Ausdruck `(E)0` erzeugt wird.  
  
> [!NOTE]
>  Namen von Enumeratoren dürfen keine Leerzeichen enthalten.  
  
 Der zugrunde liegende Typ gibt an, wie viel Speicher für jeden Enumerator reserviert wird. Eine explizite Typumwandlung ist jedoch erforderlich, um einen `enum`\-Typ in einen ganzzahligen Typ zu konvertieren. Durch die folgende Anweisung wird der `Sun`\-Enumerator beispielsweise einer Variablen des Typs [int](../../../csharp/language-reference/keywords/int.md) zugewiesen. Dabei erfolgt für die Konvertierung von `enum` in `int` eine Typumwandlung.  
  
```  
  
int x = (int)Days.Sun;  
```  
  
 Wenn <xref:System.FlagsAttribute?displayProperty=fullName> auf eine Enumeration mit Elementen angewendet wird, die mit einer bitweisen `OR`\-Operation kombiniert werden können, beeinflusst das Attribut das Verhalten von `enum` bei der Verwendung bestimmter Tools. Solche Änderungen sind bei Verwendung von Tools wie den Methoden der <xref:System.Console>\-Klasse und der Ausdrucksauswertung zu beobachten. \(Siehe das dritte Beispiel.\)  
  
## Stabile Programmierung  
 Wie bei Konstanten werden zur Kompilierzeit alle Verweise auf die einzelnen Werte einer Enumeration in numerische Literale konvertiert. Dies kann, wie unter [Konstanten](../../../csharp/programming-guide/classes-and-structs/constants.md) beschrieben, zu möglichen Versionsproblemen führen.  
  
 Das Zuweisen zusätzlicher Werte zu neuen Enumerationsversionen oder das Ändern der Werte von Enumerationsmembern in einer neuen Version kann für abhängigen Quellcode Probleme verursachen. Enumerationswerte werden oft in [switch](../../../csharp/language-reference/keywords/switch.md)\-Anweisungen verwendet. Wenn dem `enum`\-Typ weitere Elemente hinzugefügt wurden, kann der Standardabschnitt der „switch“\-Anweisung unerwartet ausgewählt werden.  
  
 Falls andere Entwickler Ihren Code verwenden, sollten Sie Richtlinien festlegen, die angeben, wie deren Code reagieren soll, wenn `enum`\-Typen neue Elemente hinzugefügt werden.  
  
## Beispiel  
 Im folgenden Beispiel wird die Enumeration `Days` deklariert. Zwei Enumeratoren werden explizit in ganze Zahlen konvertiert und „Integer“\-Variablen zugewiesen.  
  
 [!CODE [csrefKeywordsTypes#10](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#10)]  
  
## Beispiel  
 Im folgenden Beispiel wird die Basistypoption verwendet, um ein `enum` zu deklarieren, dessen Member den Typ `long` haben. Beachten Sie, dass obwohl der Enumeration der Typ `long` zugrunde liegt, die Enumerationsmember noch explizit mithilfe einer Typumwandlung in den Typ `long` umgewandelt werden müssen.  
  
 [!CODE [csrefKeywordsTypes#11](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#11)]  
  
## Beispiel  
 Im folgenden Codebeispiel werden die Verwendung des <xref:System.FlagsAttribute?displayProperty=fullName>\-Attributs in einer `enum`\-Deklaration und seine Wirkung veranschaulicht.  
  
 [!CODE [csrefKeywordsTypes#12](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#12)]  
  
## Kommentare  
 Wenn Sie `Flags` entfernen, werden im Beispiel die folgenden Werte angezeigt:  
  
 `5`  
  
 `5`  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [Enumerationstypen](../../../csharp/programming-guide/enumeration-types.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Tabelle ganzzahliger Typen](../../../csharp/language-reference/keywords/integral-types-table.md)   
 [Tabelle integrierter Typen](../../../csharp/language-reference/keywords/built-in-types-table.md)   
 [Tabelle für implizite numerische Konvertierungen](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)   
 [Tabelle für explizite numerische Konvertierungen](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)