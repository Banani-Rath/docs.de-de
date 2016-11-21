---
title: "&#220;bereinstimmungsvergleiche (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Objektgleichheit [C#]"
ms.assetid: 10b865ea-4e7b-4127-9242-c9b8f57d9f04
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &#220;bereinstimmungsvergleiche (C#-Programmierhandbuch)
Unter bestimmten Umständen ist es erforderlich, die Gleichheit zweier Werte zu prüfen.  In einigen Fällen prüfen Sie die *Wertgleichheit*, die auch als *Äquivalenz* bezeichnet wird. D. h. Sie prüfen, ob die in zwei Variablen enthaltenen Werte gleich sind.  In anderen Fällen müssen Sie ermitteln, ob zwei Variablen auf das gleiche zugrunde liegende Objekt im Arbeitsspeicher verweisen.  Diese Art von Gleichheit wird als *Verweisgleichheit* oder *Identität* bezeichnet.  In diesem Thema werden diese zwei Arten der Gleichheit beschrieben. Außerdem finden Sie hier Links zu verwandten Themen mit weiteren Informationen.  
  
## Verweisgleichheit  
 Verweisgleichheit ist gegeben, wenn zwei Objektverweise auf dasselbe zugrunde liegende Objekt verweisen.  Die Ursache hierfür kann eine einfache Zuweisung sein, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideStatements#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#18)]  
  
 In diesem Code werden zwei Objekte erstellt, nach der Zuweisungsanweisung verweisen jedoch beide Verweise auf das gleiche Objekt.  Es liegt eine Verweisgleichheit vor.  Verwenden Sie die <xref:System.Object.ReferenceEquals%2A>\-Methode, um zu ermitteln, ob zwei Verweise auf das gleiche Objekt verweisen.  
  
 Das Konzept der Verweisgleichheit gilt nur für Verweistypen.  Bei Werttypobjekten kann keine Verweisgleichheit vorliegen, da bei Zuweisung einer Werttypinstanz zu einer Variablen eine Kopie des Werts erstellt wird.  Aus diesem Grund ist es unmöglich, dass zwei nicht geschachtelte Strukturen vorhanden sind, die auf die gleiche Position im Arbeitsspeicher verweisen.  Wenn Sie zwei Werttypen mit der <xref:System.Object.ReferenceEquals%2A>\-Methode vergleichen, ist das Ergebnis immer `false`, selbst wenn die in den Objekten enthaltenen Werte alle identisch sind.  Der Grund hierfür ist, dass jede Variable in einer eigenen Objektinstanz geschachtelt ist.  Weitere Informationen finden Sie unter [Gewusst wie: Überprüfen auf Verweisgleichheit \(Identität\)](../../../csharp/programming-guide/statements-expressions-operators/how-to-test-for-reference-equality-identity.md).  
  
## Wertgleichheit  
 Eine Wertgleichheit liegt dann vor, wenn zwei Objekte den gleichen Wert bzw. die gleichen Werte enthalten.  Die Prüfung auf Wertgleichheit für primitive Werttypen wie [int](../../../csharp/language-reference/keywords/int.md) oder [bool](../../../csharp/language-reference/keywords/bool.md) ist einfach.  Sie können den [\=\=](../../../csharp/language-reference/operators/equality-comparison-operator.md)\-Operator verwenden, wie im folgenden Beispiel gezeigt.  
  
```c#  
int a = GetOriginalValue();  
int b = GetCurrentValue();  
  
// Test for value equality.   
if( b == a)   
{  
    // The two integers are equal.  
}  
```  
  
 Für die meisten anderen Typen ist die Prüfung auf Wertgleichheit komplexer, da es darauf ankommt, wie die Wertgleichheit für den jeweiligen Typ definiert wird.  Für Klassen und Strukturen mit mehreren Feldern oder Eigenschaften wird Wertgleichheit oft so definiert, dass alle Felder oder Eigenschaften den gleichen Wert aufweisen.  Zwei `Point`\-Objekte werden z. B. als äquivalent definiert, wenn pointA.X gleich pointB.X und pointA.Y gleich pointB.Y ist.  
  
 Die Äquivalenz muss jedoch nicht unbedingt auf allen Feldern in einem Typ basieren.  Die Basis kann auch eine Teilmenge sein.  Wenn Sie Typen von einem anderen Besitzer vergleichen, vergewissern Sie sich, wie die Gleichheit für den jeweiligen Typ definiert ist.  Informationen zum Definieren von Wertgleichheit für Ihre eigenen Klassen und Strukturen finden Sie unter [Gewusst wie: Definieren von Wertgleichheit für einen Typ](../../../csharp/programming-guide/statements-expressions-operators/how-to-define-value-equality-for-a-type.md).  
  
### Wertgleichheit für Gleitkommawerte  
 Die Übereinstimmungsprüfung für Gleitkommawerte \([double](../../../csharp/language-reference/keywords/double.md) und [float](../../../csharp/language-reference/keywords/float.md)\) ist aufgrund der Ungenauigkeit der Gleitkommaarithmetik auf Computern mit Binärlogik problematisch.  Weitere Informationen finden Sie in den Hinweisen im Thema <xref:System.Double?displayProperty=fullName>.  
  
## Verwandte Themen  
  
|Titel|Beschreibung|  
|-----------|------------------|  
|[Gewusst wie: Überprüfen auf Verweisgleichheit \(Identität\)](../../../csharp/programming-guide/statements-expressions-operators/how-to-test-for-reference-equality-identity.md)|Beschreibt, wie zwei Variablen auf Verweisgleichheit geprüft werden.|  
|[Gewusst wie: Definieren von Wertgleichheit für einen Typ](../../../csharp/programming-guide/statements-expressions-operators/how-to-define-value-equality-for-a-type.md)|Beschreibt, wie eine benutzerdefinierte Definition der Wertgleichheit für einen Typ erstellt wird.|  
|[C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)|Links zu ausführlichen Informationen zu wichtigen Funktionen der C\#\-Sprache sowie zu Funktionen, die über .NET Framework für C\# verfügbar sind.|  
|[Typen](../../../csharp/programming-guide/types/index.md)|Informationen zum C\#\-Typsystem und Links zu weiteren Informationen.|  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)