---
title: "Instanzkonstruktoren (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Konstruktoren [C#], Instanzkonstruktoren"
  - "Instanzkonstruktoren [C#]"
ms.assetid: 24663779-c1e5-4af4-a942-ca554e4c542d
caps.latest.revision: 26
caps.handback.revision: 26
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Instanzkonstruktoren (C#-Programmierhandbuch)
Wenn Sie mit dem Ausdruck [new](../../../csharp/language-reference/keywords/new.md) ein Objekt einer [Klasse](../../../csharp/language-reference/keywords/class.md) erstellen, werden alle Instanzmembervariablen mit Instanzkonstruktoren erstellt und initialisiert.  Um eine [statische](../../../csharp/language-reference/keywords/static.md) Klasse oder statische Variablen in einer nicht statischen Klasse zu initialisieren, müssen Sie einen statischen Konstruktor definieren.  Weitere Informationen finden Sie unter [Statische Konstruktoren](../../../csharp/programming-guide/classes-and-structs/static-constructors.md).  
  
 Im folgenden Beispiel wird ein Instanzenkonstruktor dargestellt:  
  
 [!CODE [csProgGuideObjects#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#5)]  
  
> [!NOTE]
>  Der Übersichtlichkeit halber enthält diese Klasse öffentliche Felder.  Die Verwendung von öffentlichen Feldern zum Programmieren wird nicht empfohlen, da auf diese Weise jeder Methode an einer beliebigen Stelle im Programm uneingeschränkter und ungeprüfter Zugriff auf die interne Funktionsweise eines Objekts eingeräumt wird.  Im Allgemeinen sollten Datenmember privat sein, und der Zugriff auf sie sollte ausschließlich über Klassenmethoden und Eigenschaften erfolgen.  
  
 Dieser Instanzenkonstruktor wird jedes Mal aufgerufen, wenn ein auf der `CoOrds`\-Klasse basierendes Objekt erstellt wird.  Ein Konstruktor wie dieser, der keine Argumente annimmt, wird *Standardkonstruktor* genannt.  Häufig erweist es sich jedoch als nützlich, zusätzliche Konstruktoren bereitzustellen.  Sie können beispielsweise der `CoOrds`\-Klasse einen Konstruktor hinzufügen, um die Anfangswerte für die Datenmember anzugeben:  
  
 [!CODE [csProgGuideObjects#76](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#76)]  
  
 Auf diese Weise können `CoOrd`\-Objekte mit Standardwerten oder mit bestimmten Anfangswerten erstellt werden:  
  
 [!CODE [csProgGuideObjects#77](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#77)]  
  
 Bei Klassen ohne Konstruktor wird automatisch ein Standardkonstruktor generiert, und die Objektfelder werden mit Standardwerten initialisiert.  Ein [int](../../../csharp/language-reference/keywords/int.md) wird z. B. mit 0 initialisiert.  Weitere Informationen zu Standardwerten finden Sie unter [Tabelle für Standardwerte](../../../csharp/language-reference/keywords/default-values-table.md).  Da der Standardkonstruktor der `CoOrds`\-Klasse alle Datenmember auf 0 \(null\) initialisiert, kann er einfach entfernt werden, ohne dass sich dies auf die Funktionsweise der Klasse auswirkt.  Ein vollständiges Beispiel mit mehreren Konstruktoren bietet Beispiel 1 weiter unten in diesem Thema, und in Beispiel 2 wird ein automatisch generierter Konstruktor dargestellt.  
  
 Mithilfe von Instanzkonstruktoren können Sie auch die Instanzkonstruktoren von Basisklassen aufrufen.  Der Klassenkonstruktor kann den Konstruktor der Basisklasse wie folgt über die Initialisierung aufrufen:  
  
 [!CODE [csProgGuideObjects#78](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#78)]  
  
 In diesem Beispiel übergibt die `Circle`\-Klasse Werte für den Radius und die Höhe an den Konstruktor, der von `Shape` bereitgestellt wird, wovon `Circle` abgeleitet wird.  Beispiel 3 in diesem Thema liefert ein vollständiges Beispiel mit `Shape` und `Circle`.  
  
## Beispiel 1  
 Das folgende Beispiel stellt eine Klasse mit zwei Klassenkonstruktoren dar \(einer ohne Argument und ein weiterer mit zwei Argumenten\).  
  
 [!CODE [csProgGuideObjects#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#4)]  
  
## Beispiel 2  
 In diesem Beispiel besitzt die `Person`\-Klasse keinen Konstruktor, d. h, ein Standardkonstruktor wird automatisch bereitgestellt, und die Felder werden auf ihre Standardwerte initialisiert.  
  
 [!CODE [csProgGuideObjects#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#8)]  
  
 Beachten Sie, dass `age` den Standardwert `0` und `name` den Standardwert `null` besitzt.  Weitere Informationen zu Standardwerten finden Sie unter [Tabelle für Standardwerte](../../../csharp/language-reference/keywords/default-values-table.md).  
  
## Beispiel 3  
 Das folgende Beispiel veranschaulicht die Verwendung der Basisklasseninitialisierung.  Die `Circle`\-Klasse wird von der allgemeinen `Shape`\-Klasse abgeleitet, die `Cylinder`\-Klasse wiederum von der `Circle`\-Klasse.  Der Konstruktor jeder abgeleiteten Klasse verwendet die jeweilige Basisklasseninitialisierung.  
  
 [!CODE [csProgGuideObjects#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#9)]  
  
 Weitere Beispiele zum Aufrufen von Basisklassenkonstruktoren finden Sie unter [Virtuell](../../../csharp/language-reference/keywords/virtual.md), [override](../../../csharp/language-reference/keywords/override.md) und [Basis](../../../csharp/language-reference/keywords/base.md).  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Konstruktoren](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [Destruktoren](../../../csharp/programming-guide/classes-and-structs/destructors.md)   
 [Statische](../../../csharp/language-reference/keywords/static.md)