---
title: "where (Einschr&#228;nkung des generischen Typs) (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "whereconstraint"
  - "whereconstraint_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "where (Einschränkung eines generischen Typs) [C#]"
ms.assetid: d7aa871b-0714-416a-bab2-96f87ada4310
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# where (Einschr&#228;nkung des generischen Typs) (C#-Referenz)
In einer generischen Typdefinition wird die `where`\-Klausel verwendet, um Einschränkungen für die Typen festlegen, die als Argumente für einen Typparameter verwendet werden können, der in einer generischen Deklaration definiert ist.  Eine generische Klasse, `MyGenericClass`, kann beispielsweise so deklariert werden, dass der Typparameter `T` die <xref:System.IComparable%601>\-Schnittstelle implementiert:  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
> [!NOTE]
>  Weitere Informationen über die where\-Klausel in einem Abfrageausdruck finden Sie unter [where\-Klausel](../../../csharp/language-reference/keywords/where-clause.md).  
  
 Zusätzlich zu Schnittstelleneinschränkungen kann eine `where`\-Klausel eine Basisklasseneinschränkung einschließen, die bestimmt, dass ein Typ über die angegebene Klasse als Basisklasse verfügen muss \(oder diese selbst sein muss\), damit er als Typargument für diesen generischen Typ verwendet werden kann.  Wird eine solche Einschränkung verwendet, muss sie vor jeder anderen Einschränkung für diesen Typparameter stehen.  
  
 [!CODE [csrefKeywordsContextual#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#6)]  
  
 Die `where`\-Klausel kann auch eine Konstruktoreinschränkung einschließen.  Mit dem Operator "new" ist es möglich, eine Instanz eines Typparameters zu erstellen. Hierfür muss der Typparameter allerdings durch die Konstruktoreinschränkung `new()` eingeschränkt sein.  Die [new\(\)\-Einschränkung](../../../csharp/language-reference/keywords/new-constraint.md) informiert den Compiler, dass jedes Typargument, das übergeben wird, einen zugreifbaren, parameterlosen oder Standardkonstruktor aufweisen muss.  Beispiele:  
  
 [!CODE [csrefKeywordsContextual#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#7)]  
  
 Die `new()`\-Einschränkung ist an letzter Position in der `where`\-Klausel angegeben.  
  
 Verwenden Sie bei mehreren Typparametern eine `where`\-Klausel pro Typparameter, z. B.:  
  
 [!CODE [csrefKeywordsContextual#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#8)]  
  
 Sie können auch Typparameter generischer Methoden mit Einschränkungen versehen, wie hier:  
  
```  
public bool MyMethod<T>(T t) where T : IMyInterface { }  
```  
  
 Beachten Sie, dass die Syntax zur Beschreibung von Typparametereinschränkungen in Delegaten identisch ist mit der Syntax von Methoden:  
  
```  
delegate T MyDelegate<T>() where T : new()  
```  
  
 Informationen zu generischen Delegaten finden Sie unter [Generische Delegaten](../../../csharp/programming-guide/generics/generic-delegates.md).  
  
 Details zu Syntax und Verwendung von Einschränkungen finden Sie unter [Einschränkungen für Typparameter](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md).  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Einführung in Generika](../../../csharp/programming-guide/generics/introduction-to-generics.md)   
 [new\-Einschränkung](../../../csharp/language-reference/keywords/new-constraint.md)   
 [Einschränkungen für Typparameter](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)