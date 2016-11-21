---
title: "Einf&#252;hrung in Generika (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Generika [C#], Informationen über Generika"
ms.assetid: a1ad761e-42f7-41dd-a62f-452a2de26b9d
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Einf&#252;hrung in Generika (C#-Programmierhandbuch)
Generische Klassen und Methoden kombinieren Wiederverwendbarkeit, Typsicherheit und Effizienz auf eine Weise, wie es für ihre nicht generischen Äquivalente unmöglich ist.  Generika werden am häufigsten bei Auflistungen und den Methoden zu ihrer Bearbeitung verwendet.  Version 2.0 der .NET Framework\-Klassenbibliothek stellt den neuen Namespace <xref:System.Collections.Generic> bereit, der mehrere neue, auf Generika basierende Auflistungsklassen enthält.  Alle Anwendungen, die mit [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] 2.0 oder höher arbeiten, sollten an Stelle ihrer älteren nicht generischen Entsprechungen \(z. B. <xref:System.Collections.ArrayList>\) die neuen generischen Auflistungsklassen verwenden.  Weitere Informationen finden Sie unter [Generika in der .NET Framework\-Klassenbibliothek](../../../csharp/programming-guide/generics/generics-in-the-net-framework-class-library.md).  
  
 Natürlich können Sie auch benutzerdefinierte generische Typen und Methoden erstellen, um eigene typsichere und effiziente Lösungen und Entwurfsmuster bereitzustellen.  Im folgenden Codebeispiel wird zu Demonstrationszwecken eine einfache generische Klasse mit verknüpfter Liste gezeigt.  \(In den meisten Fällen ist es ratsam, die <xref:System.Collections.Generic.List%601>\-Klasse aus der .NET Framework\-Klassenbibliothek zu verwenden, anstatt eine eigene Klasse zu schreiben.\) Der Typparameter `T` wird an mehreren Stellen verwendet, an denen der Typ des in der Liste gespeicherten Elements normalerweise durch einen konkreten Typ angegeben wird.  Er wird auf folgende Arten verwendet:  
  
-   Als Typ eines Methodenparameters in der `AddHead`\-Methode.  
  
-   Als Rückgabetyp der öffentlichen `GetNext`\-Methode und der `Data`\-Eigenschaft in der geschachtelten `Node`\-Klasse.  
  
-   Als Typ der privaten Memberdaten in der geschachtelten Klasse.  
  
 Beachten Sie, dass T in der geschachtelten `Node`\-Klasse verfügbar ist.  Wenn `GenericList<T>` mit einem konkreten Typ instanziiert wird \(beispielsweise als `GenericList<int>`\), wird jedes Vorkommen von `T` durch `int` ersetzt.  
  
 [!CODE [csProgGuideGenerics#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#2)]  
  
 Im folgenden Codebeispiel wird veranschaulicht, wie in Clientcode mithilfe der generischen `GenericList<T>`\-Klasse eine Liste mit ganzen Zahlen erstellt wird.  Allein durch Änderung des Typarguments kann der folgende Code auf einfache Weise für die Erstellung von Zeichenfolgenlisten oder Listen beliebiger benutzerdefinierter Typen angepasst werden:  
  
 [!CODE [csProgGuideGenerics#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#3)]  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Generika](../../../csharp/programming-guide/generics/index.md)