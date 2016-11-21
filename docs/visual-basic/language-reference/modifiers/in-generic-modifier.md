---
title: "In (Generic Modifier) (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.VarianceIn"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "contravariance, In keyword [Visual Basic]"
  - "In keyword [Visual Basic]"
ms.assetid: 59bb13c5-fe96-42b8-8286-86293d1661c5
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# In (Generic Modifier) (Visual Basic)
Für generische Typparameter gibt das `In`\-Schlüsselwort an, dass der Typparameter kontravariant ist.  
  
## Hinweise  
 Kontravarianz ermöglicht es, einen weniger stark abgeleiteten Typ zu verwenden als durch den generischen Parameter angegeben.  Dies ermöglicht die implizite Konvertierung von Klassen, die abweichende Schnittstellen implementieren, und die implizite Konvertierung von Delegattypen.  
  
 Weitere Informationen finden Sie unter [Kovarianz und Kontravarianz](../Topic/Covariance%20and%20Contravariance%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Regeln  
 Sie können das `In`\-Schlüsselwort in generischen Schnittstellen und Delegaten verwenden.  
  
 Ein Typparameter kann in einer generischen Schnittstelle oder einem Delegaten kontravariant deklariert werden, wenn er nur als Typ von Methodenargumenten und nicht als Methodenrückgabetyp verwendet wird.  `ByRef`\-Parameter können nicht kovariant oder kontravariant sein.  
  
 Kovarianz und Kontravarianz werden für Verweistypen, aber nicht für Werttypen unterstützt.  
  
 In Visual Basic können Sie keine Ereignisse in kontravarianten Schnittstellen deklarieren, ohne den Delegattyp anzugeben.  Kontravariante Schnittstellen können außerdem zwar geschachtelte Schnittstellen, jedoch keine geschachtelten Klassen, Enumerationen oder Strukturen aufweisen.  
  
## Verhalten  
 Eine Schnittstelle mit einem kontravarianten Typparameter ermöglicht es, dass die zugehörigen Methoden Argumente von weniger stark abgeleiteten Typen akzeptieren können als die vom Schnittstellentypparameter angegebenen.  Da in .NET Framework 4 Typ T in der <xref:System.Collections.Generic.IComparer%601>\-Schnittstelle z. B. kontravariant ist, können Sie einem Objekt des `IComparer(Of Employee)`\-Typs ein Objekt des `IComparer(Of Person)`\-Typs zuweisen, ohne spezifische Konvertierungsmethoden zu verwenden, wenn `Person` `Employee` erbt.  
  
 Einem kontravarianten Delegaten kann ein anderer Delegat desselben Typs zugewiesen werden, allerdings mit einem weniger stark abgeleiteten generischen Typparameter.  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie eine kontravariante generische Schnittstelle deklariert, erweitert und implementiert wird.  Außerdem wird gezeigt, wie Sie die implizite Konvertierung für Klassen verwenden können, die diese Schnittstelle implementieren.  
  
 [!CODE [vbVarianceKeywords#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvariancekeywords#1)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie ein kontravarianter generischer Delegat deklariert, instanziiert und aufgerufen wird.  Darüber hinaus wird gezeigt, wie Sie einen Delegattyp implizit konvertieren können.  
  
 [!CODE [vbVarianceKeywords#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvariancekeywords#2)]  
  
## Siehe auch  
 [Abweichungen bei generischen Schnittstellen](../Topic/Variance%20in%20Generic%20Interfaces%20\(C%23%20and%20Visual%20Basic\).md)   
 [Out](../../../visual-basic/language-reference/modifiers/out-generic-modifier.md)