---
title: "Generische Methoden (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "Generika [C#], Methoden"
ms.assetid: 673eeea2-4b48-4faa-9c4e-2e89449221b9
caps.latest.revision: 27
caps.handback.revision: 27
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Generische Methoden (C#-Programmierhandbuch)
Bei einer generischen Methode handelt es sich um eine mit Typparametern deklarierte Methode, wie folgt:  
  
 [!CODE [csProgGuideGenerics#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#22)]  
  
 Im folgenden Codebeispiel wird eine Möglichkeit gezeigt, die Methode mit `int` für das Typargument aufzurufen:  
  
 [!CODE [csProgGuideGenerics#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#23)]  
  
 Sie können das Typargument auch weglassen, dann wird es vom Compiler abgeleitet.  Der folgende Aufruf von `Swap` bewirkt das gleiche wie der vorherige Aufruf:  
  
 [!CODE [csProgGuideGenerics#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#24)]  
  
 Für statische Methoden und Instanzmethoden gelten die gleichen Typrückschlussregeln.  Der Compiler kann Typparameter auf der Grundlage der übergebenen Methodenargumente ableiten. Eine Einschränkung oder ein Rückgabewert genügen ihm zur Ableitung des Typparameters nicht.  Infolgedessen ist ein Typrückschluss bei Methoden ohne Parameter nicht möglich.  Der Typrückschluss tritt beim Kompilieren auf, bevor der Compiler versucht, die Signaturen von überladenen Methoden aufzulösen.  Der Compiler wendet Typrückschlusslogik auf alle generischen Methoden gleichen Namens an.  Im Schritt zur Überladungsauflösung schließt der Compiler nur die generischen Methoden ein, bei denen der Typrückschluss erfolgreich war.  
  
 Innerhalb einer generischen Klasse können nicht generische Methoden auf die Typparameter auf Klassenebene folgendermaßen zugreifen:  
  
 [!CODE [csProgGuideGenerics#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#25)]  
  
 Wenn eine generische Methode definiert wird, die die gleichen Typparameter wie die übergeordnete Klasse verwendet, gibt der Compiler die Warnung CS0693 aus, weil innerhalb des Gültigkeitsbereichs der Methode das Argument für das äußere `T` durch das Argument für das innere `T` verdeckt wird.  Falls Sie die Flexibilität benötigen, eine generische Klassenmethode mit anderen als den bei der Instanziierung der Klasse bereitgestellten Typargumenten aufrufen zu können, sollten Sie einen anderen Bezeichner für den Typparameter der Methode erwägen, wie in `GenericList2<T>` im folgenden Beispiel dargestellt.  
  
 [!CODE [csProgGuideGenerics#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#26)]  
  
 Verwenden Sie Einschränkungen, um spezialisiertere Operationen bei Typparametern in Methoden zu ermöglichen.  Diese Version von `Swap<T>`, jetzt `SwapIfGreater<T>` genannt, kann nur mit Typargumenten verwendet werden, die <xref:System.IComparable%601> implementieren.  
  
 [!CODE [csProgGuideGenerics#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#27)]  
  
 Generische Methoden können auf mehrere Typparameter überladen werden.  Beispielsweise können sich folgende Methoden alle in derselben Klasse befinden:  
  
 [!CODE [csProgGuideGenerics#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#28)]  
  
## C\#\-Programmiersprachenspezifikation  
 Weitere Informationen finden Sie unter [C\#\-Sprachspezifikation](../../../csharp/language-reference/language-specification.md).  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Einführung in Generika](../../../csharp/programming-guide/generics/introduction-to-generics.md)   
 [Methoden](../../../csharp/programming-guide/classes-and-structs/methods.md)