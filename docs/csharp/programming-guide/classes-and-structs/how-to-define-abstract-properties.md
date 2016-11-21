---
title: "Gewusst wie: Definieren von abstrakten Eigenschaften (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Abstrakte Eigenschaften [C#]"
  - "Eigenschaften [C#], abstract"
ms.assetid: 672a90eb-47b9-4ae0-9914-af53852fddcb
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Definieren von abstrakten Eigenschaften (C#-Programmierhandbuch)
Im folgenden Beispiel wird die Definition [abstrakter](../../../csharp/language-reference/keywords/abstract.md) Eigenschaften erläutert.  Die Deklaration einer abstrakten Eigenschaft stellt keine Implementierung der Eigenschaftenaccessoren bereit. Sie deklariert, dass die Klasse Eigenschaften unterstützt, überlässt die Implementierung der Accessoren jedoch abgeleiteten Klassen.  Im folgenden Beispiel wird veranschaulicht, wie die von einer Basisklasse geerbten abstrakten Eigenschaften implementiert werden.  
  
 Dieses Beispiel besteht aus drei Dateien, die einzeln kompiliert werden. Auf die sich daraus ergebende Assembly wird in der jeweils nächsten Kompilierung verwiesen:  
  
-   abstractshape.cs: Die `Shape`\-Klasse, die eine abstrakte `Area`\-Eigenschaft enthält.  
  
-   shapes.cs: Die Unterklassen der `Shape`\-Klasse.  
  
-   shapetest.cs: Ein Testprogramm zum Anzeigen der Bereiche einiger von `Shape` abgeleiteter Objekte.  
  
 Verwenden Sie zum Kompilieren des Beispiels die folgende Befehlszeile:  
  
 `csc abstractshape.cs shapes.cs shapetest.cs`  
  
 Dadurch wird die ausführbare Datei **shapetest.exe** erstellt.  
  
## Beispiel  
 Durch diese Datei wird die `Shape`\-Klasse deklariert, die die `Area`\-Eigenschaft vom Typ `double` enthält.  
  
 [!CODE [csProgGuideInheritance#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#1)]  
  
-   Modifizierer für die Eigenschaft werden in die Eigenschaftendeklaration selbst eingefügt.  Beispiele:  
  
    ```  
    public abstract double Area  
    ```  
  
-   Wenn Sie eine abstrakte Eigenschaft \(in diesem Beispiel `Area`\) deklarieren, geben Sie lediglich an, welche Eigenschaftenaccessoren verfügbar sind, ohne sie jedoch zu implementieren.  In diesem Beispiel ist nur ein [get](../../../csharp/language-reference/keywords/get.md)\-Accessor verfügbar, weswegen die Eigenschaft schreibgeschützt ist.  
  
## Beispiel  
 Im folgenden Code sind drei Unterklassen von `Shape` enthalten, die die `Area`\-Eigenschaft überschreiben, um ihre eigene Implementierung bereitzustellen.  
  
 [!CODE [csProgGuideInheritance#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#2)]  
  
## Beispiel  
 Der folgende Code stellt ein Testprogramm dar, das einige von `Shape` abgeleitete Objekte erstellt und ihre Bereiche ausgibt.  
  
 [!CODE [csProgGuideInheritance#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#3)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Abstrakte und versiegelte Klassen und Klassenmember](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md)   
 [Eigenschaften](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [Gewusst wie: Erstellen und Verwenden von Assemblys über die Befehlszeile](../Topic/How%20to:%20Create%20and%20Use%20Assemblies%20Using%20the%20Command%20Line%20\(C%23%20and%20Visual%20Basic\).md)