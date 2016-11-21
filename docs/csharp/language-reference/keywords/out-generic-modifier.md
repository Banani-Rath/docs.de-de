---
title: "out (generischer Modifizierer) (C#-Referenz) | Microsoft Docs"
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
  - "Kovarianz, out-Schlüsselwort [C#]"
  - "out-Schlüsselwort [C#]"
ms.assetid: f8c20dec-a8bc-426a-9882-4076b1db1e00
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# out (generischer Modifizierer) (C#-Referenz)
Für generische Typparameter gibt das `out`\-Schlüsselwort an, dass der Typparameter kovariant ist.  Sie können das `out`\-Schlüsselwort in generischen Schnittstellen und Delegaten verwenden.  
  
 Kovarianz ermöglicht es, einen stärker abgeleiteten Typ zu verwenden als durch den generischen Parameter angegeben.  Dies ermöglicht die implizite Konvertierung von Klassen, die abweichende Schnittstellen implementieren, und die implizite Konvertierung von Delegattypen.  Kovarianz und Kontravarianz werden für Verweistypen, aber nicht für Werttypen unterstützt.  
  
 Eine Schnittstelle, die über einen kovarianten Typparameter verfügt, ermöglicht es den zugehörigen Methoden, mehr abgeleitete Typen zurückzugeben als vom Typparameter angegeben.  Da in .NET Framework 4 beispielsweise Typ T in <xref:System.Collections.Generic.IEnumerable%601> kovariant ist, können Sie einem Objekt des Typs `IEnumerable(Of Object)` ein Objekt des Typs `IEnumerabe(Of String)` zuweisen, ohne besondere Konvertierungsmethoden zu verwenden.  
  
 Einem kovarianten Delegaten kann ein anderer Delegat desselben Typs zugewiesen werden, allerdings mit einem stärker abgeleiteten generischen Typparameter.  
  
 Weitere Informationen finden Sie unter [Kovarianz und Kontravarianz](../Topic/Covariance%20and%20Contravariance%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie eine kovariante generische Schnittstelle deklariert, erweitert und implementiert wird.  Außerdem wird gezeigt, wie die implizite Konvertierung für Klassen verwendet wird, die eine kovariante Schnittstelle implementieren.  
  
 [!CODE [csVarianceKeywords#3](../CodeSnippet/VS_Snippets_VBCSharp/csvariancekeywords#3)]  
  
 In einer generischen Schnittstelle kann ein Typparameter kovariant deklariert werden, wenn er die folgenden Bedingungen erfüllt:  
  
-   Der Typparameter wird nur als Rückgabetyp von Schnittstellenmethoden und nicht als Typ von Methodenargumenten verwendet.  
  
    > [!NOTE]
    >  Es gibt allerdings eine Ausnahme zu dieser Regel.  Wenn eine kovariante Schnittstelle einen kontravarianten generischen Delegaten als Methodenparameter enthält, können Sie den kovarianten Typ als generischen Typparameter für diesen Delegaten verwenden.  Weitere Informationen über kovariante und kontravariante generische Delegaten finden Sie unter [Varianz bei Delegaten](../Topic/Variance%20in%20Delegates%20\(C%23%20and%20Visual%20Basic\).md) und [Verwenden von Varianz für die generischen Delegaten Func und Action](../Topic/Using%20Variance%20for%20Func%20and%20Action%20Generic%20Delegates%20\(C%23%20and%20Visual%20Basic\).md).  
  
-   Der Typparameter wird nicht als generische Einschränkung für die Schnittstellenmethoden verwendet.  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie ein kovarianter generischer Delegat deklariert, instanziiert und aufgerufen wird.  Außerdem wird gezeigt, wie Delegattypen implizit konvertiert werden.  
  
 [!CODE [csVarianceKeywords#4](../CodeSnippet/VS_Snippets_VBCSharp/csvariancekeywords#4)]  
  
 In einem generischen Delegaten kann ein Typ kovariant deklariert werden, wenn er nur als Methodenrückgabetyp und nicht für Methodenargumente verwendet wird.  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [Abweichungen bei generischen Schnittstellen](../Topic/Variance%20in%20Generic%20Interfaces%20\(C%23%20and%20Visual%20Basic\).md)   
 [in](../../../csharp/language-reference/keywords/in-generic-modifier.md)   
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)