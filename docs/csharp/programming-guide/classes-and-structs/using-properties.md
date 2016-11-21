---
title: "Verwenden von Eigenschaften (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Get-Accessor [C#]"
  - "Eigenschaften [C#], Informationen über Eigenschaften"
  - "Set-Accessor [C#]"
ms.assetid: f7f67b05-0983-4cdb-96af-1855d24c967c
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Verwenden von Eigenschaften (C#-Programmierhandbuch)
Eigenschaften beinhalten sowohl Aspekte von Feldern als auch von Methoden.  Dem Benutzer eines Objekts erscheint eine Eigenschaft wie ein Feld. Um auf die Eigenschaft zugreifen zu können, ist dieselbe Syntax erforderlich.  Für den Implementierer einer Klasse besteht eine Eigenschaft aus einem oder zwei Codeblöcken, die einen [get](../../../csharp/language-reference/keywords/get.md)\-Accessor und\/oder einen [set](../../../csharp/language-reference/keywords/set.md)\-Accessor darstellen.  Der Codeblock für den `get`\-Accessor wird ausgeführt, wenn die Eigenschaft gelesen wird. Der Codeblock für den `set`\-Accessor wird ausgeführt, wenn der Eigenschaft ein neuer Wert zugeordnet wird.  Eine Eigenschaft ohne einen `set`\-Accessor gilt als schreibgeschützt.  Eine Eigenschaft ohne einen `get`\-Accessor gilt als lesegeschützt.  Eine Eigenschaft mit beiden Accessoren ermöglicht Lese\- und Schreibzugriff.  
  
 Im Gegensatz zu Feldern werden Eigenschaften nicht als Variablen klassifiziert.  Aus diesem Grund können Sie Eigenschaften nicht als Parameter [ref](../../../csharp/language-reference/keywords/ref.md) oder [out](../../../csharp/language-reference/keywords/out.md) übergeben.  
  
 Eigenschaften haben viele Verwendungszwecke: Sie können Daten überprüfen, bevor eine Änderung zugelassen wird. Sie können Daten in einer Klasse auf transparente Weise verfügbar machen, wobei diese Daten in Wirklichkeit von einer anderen Quelle abgefragt werden, z. B. einer Datenbank. Sie können eine Aktion durchführen, wenn Daten verändert werden, z. B. ein Ereignis auslösen oder Werte anderer Felder verändern.  
  
 Eigenschaften werden innerhalb des Klassenblocks definiert, indem die Zugriffsebene des Felds angegeben wird, gefolgt vom Typ und dem Namen der Eigenschaft sowie von einem Codeblock, der einen `get`\-Accessor und\/oder einen `set`\-Accessor deklariert.  Beispiele:  
  
 [!CODE [csProgGuideProperties#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#7)]  
  
 In diesem Beispiel wird `Month` als Eigenschaft deklariert, damit der `set`\-Accessor dafür sorgen kann, dass der `Month`\-Wert zwischen 1 und 12 festgelegt wird.  Die `Month`\-Eigenschaft verwendet ein privates Feld für die Nachverfolgung des tatsächlichen Werts.  Der tatsächliche Speicherort, an dem die Daten einer Eigenschaft gespeichert werden, wird oft als "Sicherungsspeicher" der Eigenschaft bezeichnet. Es ist üblich, dass Eigenschaften private Felder als Sicherungsspeicher verwenden.  Das Feld wird als privat gekennzeichnet, damit sichergestellt ist, dass eine Änderung des Felds nur durch Aufrufen der Eigenschaft durchgeführt werden kann.  Weitere Informationen über öffentliche und private Zugriffsbeschränkungen finden Sie unter [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).  
  
 Automatisch implementierte Eigenschaften stellen vereinfachte Syntax für einfache Eigenschaftendeklarationen bereit.  Weitere Informationen finden Sie unter [Automatisch implementierte Eigenschaften](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).  
  
## get\-Accessor  
 Der Text des `get`\-Accessors ähnelt dem Text einer Methode.  Er muss einen Wert des Eigenschaftentyps zurückgeben.  Die Ausführung des `get`\-Accessors entspricht dem Lesen des Feldwerts.  Wenn Sie z. B. die private Variable von dem `get`\-Accessor zurückgeben und Optimierungen aktiviert sind, wird der Aufruf an die `get`\-Accessormethode durch den Compiler eingebettet, damit kein zusätzlicher Aufwand an Methodenaufrufen entsteht.  Eine virtuelle `get`\-Accessormethode kann jedoch nicht eingebettet werden, da zur Kompilierzeit im Compiler nicht bekannt ist, welche Methode während der Laufzeit tatsächlich aufgerufen wird.  Das folgende Beispiel enthält einen `get`\-Accessor, der den Wert des privaten Felds `name` zurückgibt:  
  
 [!CODE [csProgGuideProperties#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#8)]  
  
 Wenn Sie auf die Eigenschaft verweisen \(außer als Ziel einer Anweisung\), wird der `get`\-Accessor aufgerufen, um den Wert der Eigenschaft zu lesen.  Beispiele:  
  
 [!CODE [csProgGuideProperties#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#9)]  
  
 Der `get`\-Accessor muss mit einer [return](../../../csharp/language-reference/keywords/return.md)\-Anweisung oder einer [throw](../../../csharp/language-reference/keywords/throw.md)\-Anweisung enden, und die Steuerung darf nicht über den Accessortext hinausgehen.  
  
 Beim Programmieren sollte vermieden werden, den Zustand des Objekts mit dem `get`\-Accessor zu ändern.  Der folgende Accessor hat beispielsweise den Nebeneffekt, dass der Zustand des Objekts bei jedem Zugriff auf das `number`\-Feld geändert wird.  
  
 [!CODE [csProgGuideProperties#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#10)]  
  
 Der `get`\-Accessor kann verwendet werden, um entweder den Feldwert zurückzugeben oder um den Feldwert zu berechnen und zurückzugeben.  Beispiele:  
  
 [!CODE [csProgGuideProperties#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#11)]  
  
 Wenn Sie der `Name`\-Eigenschaft im vorangehenden Codesegment keinen Wert zuweisen, wird der Wert NA zurückgegeben.  
  
## set\-Accessor  
 Der `set`\-Accessor kann mit einer Methode verglichen werden, deren Rückgabetyp [void](../../../csharp/language-reference/keywords/void.md) ist.  Er verwendet einen impliziten Parameter mit der Bezeichnung `value`, dessen Typ dem Typ der Eigenschaft entspricht.  Im folgenden Beispiel wird ein `set`\-Accessor der `Name`\-Eigenschaft hinzugefügt:  
  
 [!CODE [csProgGuideProperties#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#12)]  
  
 Wenn Sie der Eigenschaft einen Wert zuweisen, wird der `set`\-Accessor mit einem Argument aufgerufen, das den neuen Wert angibt.  Beispiele:  
  
 [!CODE [csProgGuideProperties#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#13)]  
  
 Es wäre falsch, den impliziten Parameternamen \(`value`\) für die Deklaration einer lokalen Variablen in einem `set`\-Accessor zu verwenden.  
  
## Hinweise  
 Eigenschaften können als `public`, `private`, `protected`, `internal` und `protected internal` gekennzeichnet sein.  Diese Zugriffsmodifizierer definieren, wie Benutzer der Klasse auf die Eigenschaft zugreifen können.  Der `get`\-Accessor und der `set`\-Accessor haben für die gleiche Eigenschaft möglicherweise verschiedene Zugriffsmodifizierer.  So kann `get` zum Beispiel `public` sein, um den schreibgeschützten Zugriff von außerhalb des Typs zuzulassen, und `set` kann möglicherweise `private` oder `protected` sein.  Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).  
  
 Eine Eigenschaft kann mit dem `static`\-Schlüsselwort als statische Eigenschaft deklariert werden.  Dadurch ist die Eigenschaft jederzeit für Aufrufer verfügbar, selbst wenn keine Instanz der Klasse vorhanden ist.  Weitere Informationen finden Sie unter [Statische Klassen und statische Klassenmember](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  
  
 Eine Eigenschaft kann mit dem [virtual](../../../csharp/language-reference/keywords/virtual.md)\-Schlüsselwort als virtuelle Eigenschaft gekennzeichnet werden.  Dies ermöglicht abgeleiteten Klassen, das Verhalten von Eigenschaften mit dem [override](../../../csharp/language-reference/keywords/override.md)\-Schlüsselwort zu überschreiben.  Weitere Informationen zum Ändern dieser Optionen finden Sie unter [Vererbung](../../../csharp/programming-guide/classes-and-structs/inheritance.md).  
  
 Eine Eigenschaft, die eine virtuelle Eigenschaft überschreibt, kann ebenfalls [sealed](../../../csharp/language-reference/keywords/sealed.md) sein. Damit ist sie für abgeleitete Klassen nicht mehr virtuell.  Und nicht zuletzt kann eine Eigenschaft als [abstract](../../../csharp/language-reference/keywords/abstract.md) deklariert werden.  Dies bedeutet, dass die Klasse keine Implementierung enthält, sodass abgeleitete Klassen eine eigene Implementierung schreiben müssen.  Weitere Informationen zum Ändern dieser Optionen finden Sie unter [Abstrakte und versiegelte Klassen und Klassenmember](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md).  
  
> [!NOTE]
>  Es wird ein Fehler verursacht, wenn einer der Modifizierer [Virtuell](../../../csharp/language-reference/keywords/virtual.md), [abstract](../../../csharp/language-reference/keywords/abstract.md) oder [override](../../../csharp/language-reference/keywords/override.md) für einen Accessor einer [static](../../../csharp/language-reference/keywords/static.md)\-Eigenschaft verwendet wird.  
  
## Beispiel  
 Dieses Beispiel veranschaulicht die Verwendung von Instanzeigenschaften, statischen Eigenschaften und Nur\-Lesen\-Eigenschaften.  Die Eingabe des Mitarbeiternamens über die Tastatur wird akzeptiert, `NumberOfEmployees` wird um 1 erhöht, und der Name sowie die Nummer des Mitarbeiters werden angezeigt.  
  
 [!CODE [csProgGuideProperties#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#2)]  
  
## Beispiel  
 Dieses Beispiel zeigt, wie auf eine Eigenschaft in einer Basisklasse zugegriffen wird, die durch eine andere Eigenschaft mit demselben Namen in einer abgeleiteten Klasse verborgen wird.  
  
 [!CODE [csProgGuideProperties#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#3)]  
  
 Im Folgenden werden einige wichtige Aspekte erläutert, die im oben aufgeführten Beispiel enthalten sind:  
  
-   Die `Name`\-Eigenschaft in der Basisklasse wird durch die `Name`\-Eigenschaft in der abgeleiteten Klasse verborgen.  In einem solchen Fall wird der `new`\-Modifizierer für die Deklaration der Eigenschaft in der abgeleiteten Klasse verwendet:  
  
     [!CODE [csProgGuideProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#4)]  
  
-   Die Umwandlung `(Employee)` wird verwendet, um auf die verborgene Eigenschaft in der Basisklasse zuzugreifen:  
  
     [!CODE [csProgGuideProperties#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#5)]  
  
     Weitere Informationen zum Ausblenden von Membern finden Sie unter [new\-Modifizierer](../../../csharp/language-reference/keywords/new-modifier.md).  
  
## Beispiel  
 In diesem Beispiel wird durch die beiden Klassen `Cube` und `Square` die abstrakte `Shape`\-Klasse implementiert. Zusätzlich wird deren abstrakte `Area`\-Eigenschaft überschrieben.  Beachten Sie die Verwendung des [override](../../../csharp/language-reference/keywords/override.md)\-Modifizierers für die Eigenschaften.  Die Seitenlänge wird vom Programm als Eingabe akzeptiert, und die Oberfläche des Quadrats und des Würfels werden berechnet.  Auch die Oberfläche wird als Eingabe akzeptiert, und die entsprechende Seitenlänge des Quadrats und des Würfels wird berechnet.  
  
 [!CODE [csProgGuideProperties#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#6)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Eigenschaften](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Schnittstelleneigenschaften](../../../csharp/programming-guide/classes-and-structs/interface-properties.md)   
 [Automatisch implementierte Eigenschaften](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md)