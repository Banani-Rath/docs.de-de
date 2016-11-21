---
title: "in (generischer Modifizierer) (C#-Referenz) | Microsoft Docs"
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
  - "Kontravarianz, in-Schlüsselwort [C#]"
  - "in-Schlüsselwort [C#]"
ms.assetid: 3a778c36-8aed-4ebe-aa8b-39f4057215b1
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# in (generischer Modifizierer) (C#-Referenz)
Für generische Typparameter gibt das `in`\-Schlüsselwort an, dass der Typparameter kontravariant ist.  Sie können das `in`\-Schlüsselwort in generischen Schnittstellen und Delegaten verwenden.  
  
 Kontravarianz ermöglicht es, einen weniger stark abgeleiteten Typ zu verwenden als durch den generischen Parameter angegeben.  Dies ermöglicht die implizite Konvertierung von Klassen, die abweichende Schnittstellen implementieren, und die implizite Konvertierung von Delegattypen.  Kovarianz und Kontravarianz in generischen Typparametern werden für Verweistypen, aber nicht für Werttypen unterstützt.  
  
 Ein Typ kann in einer generischen Oberfläche oder einem generischen Delegaten kovariant deklariert werden, wenn er nur als Typ von Methodenargumenten und nicht als Methodenrückgabetyp verwendet wird.  Der `Ref`\-Parameter und der `out`\-Parameter können kein Variant sein.  
  
 Eine Schnittstelle mit einem kontravarianten Typparameter ermöglicht es, dass die zugehörigen Methoden Argumente von weniger stark abgeleiteten Typen akzeptieren können als die vom Schnittstellentypparameter angegebenen.  Da in .NET Framework 4 Typ T in der <xref:System.Collections.Generic.IComparer%601>\-Schnittstelle z. B. kontravariant ist, können Sie einem Objekt des `IComparer(Of Employee)`\-Typs ein Objekt des `IComparer(Of Person)`\-Typs zuweisen, ohne spezifische Konvertierungsmethoden zu verwenden, wenn `Employee` `Person` erbt.  
  
 Einem kontravarianten Delegaten kann ein anderer Delegat desselben Typs zugewiesen werden, allerdings mit einem weniger stark abgeleiteten generischen Typparameter.  
  
 Weitere Informationen finden Sie unter [Kovarianz und Kontravarianz](../Topic/Covariance%20and%20Contravariance%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie eine kontravariante generische Schnittstelle deklariert, erweitert und implementiert wird.  Außerdem wird gezeigt, wie Sie die implizite Konvertierung für Klassen verwenden können, die diese Schnittstelle implementieren.  
  
 [!CODE [csVarianceKeywords#1](../CodeSnippet/VS_Snippets_VBCSharp/csvariancekeywords#1)]  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie ein kontravarianter generischer Delegat deklariert, instanziiert und aufgerufen wird.  Darüber hinaus wird gezeigt, wie Sie einen Delegattyp implizit konvertieren können.  
  
 [!CODE [csVarianceKeywords#2](../CodeSnippet/VS_Snippets_VBCSharp/csvariancekeywords#2)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [out](../../../csharp/language-reference/keywords/out-generic-modifier.md)   
 [Kovarianz und Kontravarianz](../Topic/Covariance%20and%20Contravariance%20\(C%23%20and%20Visual%20Basic\).md)   
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)