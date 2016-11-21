---
title: "Gewusst wie: Verwenden von Lambda-Ausdr&#252;cken au&#223;erhalb von LINQ (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Lambda-Ausdrücke [C#], Außerhalb von LINQ"
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden von Lambda-Ausdr&#252;cken au&#223;erhalb von LINQ (C#-Programmierhandbuch)
Lambda\-Ausdrücke sind nicht auf [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)]\-Abfragen beschränkt.  Sie können überall dort verwendet werden, wo ein Delegatwert erwartet wird, also da, wo anonyme Methoden eingesetzt werden können.  Das folgende Beispiel veranschaulicht die Verwendung eines Lambda\-Ausdrucks in einem Windows Forms\-Ereignishandler.  Beachten Sie, dass die Eingabetypen \(<xref:System.Object> und <xref:System.Windows.Forms.MouseEventArgs>\) vom Compiler abgeleitet werden und nicht explizit in den Lambda\-Eingabeparametern angegeben werden müssen.  
  
## Beispiel  
  
```  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## Siehe auch  
 [Lambda\-Ausdrücke](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)   
 [Anonyme Methoden](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)   
 [LINQ \(Language\-Integrated Query\)](../Topic/LINQ%20\(Language-Integrated%20Query\).md)