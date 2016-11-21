---
title: "Generische Klassen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "C#-Sprache, Generische Klassen"
  - "Generika [C#], Klassen"
ms.assetid: 27d6f256-cd61-41e3-bc6e-b990a53b0224
caps.latest.revision: 30
caps.handback.revision: 30
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Generische Klassen (C#-Programmierhandbuch)
Generische Klassen kapseln Operationen, die nicht spezifisch für einen bestimmten Datentyp sind.  Generische Klassen werden am häufigsten bei Auflistungen verwendet, z. B. bei verknüpften Listen, Hashtabellen, Stapeln, Warteschlangen, Strukturen usw.  Vorgänge wie das Hinzufügen oder Entfernen von Elementen aus der Auflistung werden nahezu auf die gleiche Art und Weise ausgeführt, unabhängig vom Typ der gespeicherten Daten.  
  
 Für die meisten Szenarios, die Auflistungsklassen erfordern, wird empfohlen, die in der Klassenbibliothek von .NET Framework 2.0 bereitgestellten Auflistungsklassen zu verwenden.  Weitere Informationen zur Verwendung dieser Klassen finden Sie unter [Generika in der .NET Framework\-Klassenbibliothek](../../../csharp/programming-guide/generics/generics-in-the-net-framework-class-library.md).  
  
 In der Regel erstellen Sie generische Klassen, indem Sie von einer vorhandenen konkreten Klasse ausgehen und Typen in Typparameter ändern \(einen nach dem anderen\), bis das optimale Verhältnis zwischen Verallgemeinerung und Verwendbarkeit gefunden ist.  Wenn Sie eigene generische Klassen erstellen möchten, sollten Sie die folgenden wichtigen Aspekte beachten:  
  
-   Welche Typen sollen in Typparameter verallgemeinert werden.  
  
     Im Allgemeinen gilt: Je mehr Typen Sie parametrisieren können, umso flexibler und besser wiederverwendbar ist Ihr Code.  Jedoch kann ein Zuviel an Verallgemeinerung zu Code führen, der von anderen Entwicklern nur schwer gelesen oder verstanden wird.  
  
-   Welche Einschränkungen sollen ggf. auf die Typparameter angewendet werden \(siehe [Einschränkungen für Typparameter](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)\).  
  
     Es empfiehlt sich, alle Einschränkungen anzuwenden, die maximal möglich sind, und bei denen Sie dennoch sämtliche Typen, die Sie behandeln müssen, auch behandeln können.  Wenn Sie zum Beispiel wissen, dass die generische Klasse nur mit Referenztypen verwendet werden soll, dann können Sie die Klasseneinschränkung anwenden.  Dadurch wird verhindert, dass die Klasse unbeabsichtigt mit Werttypen verwendet wird. Gleichzeitig können Sie den Operator `as` für `T` verwenden und nach NULL\-Werten suchen.  
  
-   Ob das generische Verhalten in Basisklassen und Unterklassen zerlegt werden soll.  
  
     Da generische Klassen als Basisklassen dienen können, sind hier beim Entwurf die gleichen Aspekte zu berücksichtigen wie bei nicht generischen Klassen.  Weitere Informationen bieten die Regeln zum Erben von generischen Basisklassen weiter unten in diesem Thema.  
  
-   Ob eine oder mehrere generische Schnittstellen implementiert werden soll.  
  
     Wenn Sie beispielsweise eine Klasse entwerfen, die zum Erstellen von Elementen in einer generisch basierten Auflistung verwendet wird, müssen Sie unter Umständen eine Schnittstelle implementieren, z. B. <xref:System.IComparable%601>, wobei `T` der Typ Ihrer Klasse ist.  
  
 Ein Beispiel für eine einfache generische Klasse finden Sie unter [Einführung in Generika](../../../csharp/programming-guide/generics/introduction-to-generics.md).  
  
 Die Regeln für Einschränkungen und Typparameter haben eine Reihe von Auswirkungen auf das Verhalten einer generischen Klasse, besonders im Hinblick auf Vererbung und Zugriff der Member.  Bevor Sie fortfahren, sollten Sie einige Begriffe verstehen.  Bei einer generischen Klasse kann der `Node<T>,`\-Clientcode auf die Klasse verweisen, indem er ein Typargument angibt, um einen geschlossenen konstruierten Typ zu erstellen \(`Node<int>`\).  Die Alternative besteht darin, den Typparameter nicht anzugeben, z. B. wenn Sie eine generische Basisklasse angeben, um einen offenen konstruierten Typ \(`Node<T>`\) zu erstellen.  Generische Klassen können von konkreten, geschlossenen konstruierten oder offenen konstruierten Basisklassen erben:  
  
 [!CODE [csProgGuideGenerics#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#16)]  
  
 Nicht generische, d. h. konkrete Klassen können von geschlossenen konstruierten Basisklassen erben, aber nicht von offenen konstruierten Klassen oder Typparametern, denn während der Laufzeit ist es für den Clientcode nicht möglich, das erforderliche Typargument bereitzustellen, das zum Instanziieren der Basisklasse benötigt wird.  
  
 [!CODE [csProgGuideGenerics#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#17)]  
  
 Generische Klassen, die von offenen konstruierten Typen erben, müssen für sämtliche Basisklassen\-Typparameter, die von der erbenden Klasse nicht verwendet werden, Typargumente bereitstellen. Der folgende Code stellt ein Beispiel dafür dar:  
  
 [!CODE [csProgGuideGenerics#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#18)]  
  
 Generische Klassen, die von offenen konstruierten Typen erben, müssen Einschränkungen angeben, die den Einschränkungen des Basistyps übergeordnet sind oder diese implizieren.  
  
 [!CODE [csProgGuideGenerics#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#19)]  
  
 Generische Typen können mehrere Typparameter und Einschränkungen verwenden. Beispiel:  
  
 [!CODE [csProgGuideGenerics#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#20)]  
  
 Offene konstruierte und geschlossene konstruierte Typen können als Methodenparameter verwendet werden:  
  
 [!CODE [csProgGuideGenerics#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#21)]  
  
 Wenn eine generische Klasse eine Schnittstelle implementiert, können alle Instanzen dieser Klasse in diese Schnittstelle umgewandelt werden.  
  
 Generische Klassen sind unveränderlich.  Dies bedeutet: Wenn ein Eingabeparameter eine `List<BaseClass>` angibt, wird Ihnen ein Kompilierungsfehler angezeigt, falls Sie versuchen, eine `List<DerivedClass>` bereitzustellen.  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Generika](../../../csharp/programming-guide/generics/index.md)   
 [Speichern des Zustands von Enumeratoren](http://go.microsoft.com/fwlink/?LinkId=112390)   
 [Ein Vererbungs\-Puzzle, Teil 1](http://go.microsoft.com/fwlink/?LinkId=112380)