---
title: "&#220;berladbare Operatoren (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "C#-Sprache, Operatoren überladen"
  - "Überladen von Operatoren [C#]"
ms.assetid: 390d9d01-79fc-40ab-9ed3-0bf448da1b6a
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# &#220;berladbare Operatoren (C#-Programmierhandbuch)
C\# ermöglicht benutzerdefinierten Typen, mithilfe des Schlüsselworts [operator](../../../csharp/language-reference/keywords/operator.md) Operatoren durch das Definieren von statischen Memberfunktionen zu überladen.  Nicht alle Operatoren können überladen werden und weisen andere Einschränkungen auf. Eine entsprechende Auflistung finden Sie in dieser Tabelle:  
  
|Operatoren|Überladbarkeit|  
|----------------|--------------------|  
|[\+](../../../csharp/language-reference/operators/addition-operator.md), [\-](../../../csharp/language-reference/operators/subtraction-operator.md), [\!](../../../csharp/language-reference/operators/logical-negation-operator.md), [~](../../../csharp/language-reference/operators/bitwise-complement-operator.md), [\+\+](../../../csharp/language-reference/operators/increment-operator.md), [\-\-](../../../csharp/language-reference/operators/decrement-operator.md), [true](../../../csharp/language-reference/keywords/true.md), [false](../../../csharp/language-reference/keywords/false.md)|Diese unären Operatoren können überladen werden.|  
|[\+](../../../csharp/language-reference/operators/addition-operator.md), [\-](../../../csharp/language-reference/operators/subtraction-operator.md), [\*](../../../csharp/language-reference/operators/multiplication-operator.md), [\/](../../../csharp/language-reference/operators/division-operator.md), [%](../../../csharp/language-reference/operators/modulus-operator.md), [&](../../../csharp/language-reference/operators/and-operator.md),                               [&#124;](../../../csharp/language-reference/operators/or-operator.md) , [^](../../../csharp/language-reference/operators/xor-operator.md), [\<\<](../../../csharp/language-reference/operators/left-shift-operator.md), [\>\>](../../../csharp/language-reference/operators/right-shift-operator.md)|Diese binären Operatoren können überladen werden.|  
|[\=\=](../../../csharp/language-reference/operators/equality-comparison-operator.md), [\!\=](../../../csharp/language-reference/operators/not-equal-operator.md), [\<](../../../csharp/language-reference/operators/less-than-operator.md), [\>](../../../csharp/language-reference/operators/greater-than-operator.md), [\<\=](../../../csharp/language-reference/operators/less-than-equal-operator.md), [\>\=](../../../csharp/language-reference/operators/greater-than-equal-operator.md)|Die Vergleichsoperatoren können überladen \(beachten Sie jeden Hinweis im Anschluss an diese Tabelle\) werden.|  
|[&&](../../../csharp/language-reference/operators/conditional-and-operator.md), [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md)|Die bedingten logischen Operatoren können nicht überladen werden. Sie werden jedoch mithilfe von `&` und                               `&#124;` ausgewertet. Selbige können überladen werden.|  
|[&#91;&#93;](../../../csharp/language-reference/operators/index-operator.md)|Der Arrayindizierungsoperator kann nicht überladen werden. Sie können jedoch Indexer definieren.|  
|[\(T\)x](../../../csharp/language-reference/operators/invocation-operator.md)|Der Umwandlungsoperator kann nicht überladen werden. Sie können jedoch neue Konvertierungsoperatoren \(siehe [explizit](../../../csharp/language-reference/keywords/explicit.md) und [implizit](../../../csharp/language-reference/keywords/implicit.md)\) definieren.|  
|[\+\=](../../../csharp/language-reference/operators/addition-assignment-operator.md), [\-\=](../../../csharp/language-reference/operators/subtraction-assignment-operator-1.md), [\*\=](../../../csharp/language-reference/operators/multiplication-assignment-operator.md), [\/\=](../../../csharp/language-reference/operators/subtraction-assignment-operator.md), [%\=](../../../csharp/language-reference/operators/modulus-assignment-operator.md), [&\=](../../../csharp/language-reference/operators/and-assignment-operator.md), [&#124;\=](../../../csharp/language-reference/operators/or-assignment-operator.md), [^\=](../../../csharp/language-reference/operators/xor-assignment-operator.md), [\<\<\=](../../../csharp/language-reference/operators/left-shift-assignment-operator.md), [\>\>\=](../../../csharp/language-reference/operators/right-shift-assignment-operator.md)|Zuweisungsoperatoren können nicht überladen werden. `+=` wird jedoch beispielsweise mithilfe von `+` ausgewertet, was wiederum überladen werden kann.|  
|[\=](../../../csharp/language-reference/operators/assignment-operator.md), [.](../../../csharp/language-reference/operators/member-access-operator.md), [?:](../../../csharp/language-reference/operators/conditional-operator.md), [??](../../../csharp/language-reference/operators/null-conditional-operator.md), [\-\>](../../../csharp/language-reference/operators/dereference-operator.md), [\=\>](../../../csharp/language-reference/operators/lambda-operator.md), [f\(x\)](../../../csharp/language-reference/operators/invocation-operator.md), [as](../../../csharp/language-reference/keywords/as.md), [checked](../../../csharp/language-reference/keywords/checked.md), [unchecked](../../../csharp/language-reference/keywords/unchecked.md), [default](../../../csharp/programming-guide/generics/default-keyword-in-generic-code.md), [delegate](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md), [is](../../../csharp/language-reference/keywords/is.md), [new](../../../csharp/language-reference/keywords/new.md), [sizeof](../../../csharp/language-reference/keywords/sizeof.md), [typeof](../../../csharp/language-reference/keywords/typeof.md)|Diese Operatoren können nicht überladen werden.|  
  
> [!NOTE]
>  Die Vergleichsoperatoren müssen, sofern sie überladen sind, paarweise überladen werden. Beim Überladen von `==` muss `!=` demnach ebenfalls überladen werden.  Das gilt auch umgekehrt, und Ähnliches gilt für `<` und `>` sowie für `<=` und `>=`.  
  
 Für das Überladen eines Operators in einer benutzerdefinierten Klasse muss eine Methode in der Klasse mit der richtigen Signatur erstellt werden.  Die Methode muss als „operator X“ bezeichnet werden, wobei X für den Namen oder das Symbol des zu überladenden Operators steht.  Unäre Operatoren verfügen über einen Parameter. Demgegenüber weisen binäre Operatoren zwei Parameter auf.  In jedem Fall muss ein Parameter denselben Typ wie die Klasse oder Struktur aufweisen, die den Operator deklariert.  
  
```c#  
public static Complex operator +(Complex c1, Complex c2)  
    {  
        Return new Complex(c1.real + c2.real, c1.imaginary + c2.imaginary);  
    }  
  
```  
  
 Es ist üblich, Definitionen zu verwenden, die umgehend das Ergebnis des Ausdrucks zurückgeben.  Es gibt eine Syntaxabkürzung mithilfe von `=>` für diese Situationen  
  
```c#  
public static Complex operator +(Complex c1, Complex c2) =>  
        new Complex(c1.real + c2.real, c1.imaginary + c2.imaginary);  
  
    // Override ToString() to display a complex number   
    // in the traditional format:  
    public override string ToString() => $"{this.real} + {this.imaginary}";  
  
```  
  
 Weitere Informationen finden Sie unter [Gewusst wie: Verwenden der Operatorüberladung zum Erstellen einer Klasse für komplexe Zahlen](../../../csharp/programming-guide/statements-expressions-operators/how-to-use-operator-overloading-to-create-a-complex-number-class.md).  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Anweisungen, Ausdrücke und Operatoren](../../../csharp/programming-guide/statements-expressions-operators/index.md)   
 [Operatoren](../../../csharp/programming-guide/statements-expressions-operators/operators.md)   
 [C\#\-Operatoren](../../../csharp/language-reference/operators/index.md)   
 [Warum sind überladene Operatoren in C\# immer statisch?](http://go.microsoft.com/fwlink/?LinkId=112383)